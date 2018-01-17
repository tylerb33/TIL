### Numeric Functions

* SELECT ( 1 + 1); returns 2
* SELECT ( 1 + 1.0); returns 2.0
* SELECT TYPEOF ( 1 + 1.0 ); returns real
<!-- If you use the + sign, TYPEOF will return integer even if strings are used. '+' assumes they are integers. -->

SELECT 1 / 2; returns 0
SELECT CASE(1 AS REAL) / 2; returns .5 which is accurate
SELECT 17 / 5; returns 3
SELECT 17 / 5, 17 % 5; returns 3 and 2 (the remainder);
SELECT ROUND(2.55555); returns 3.0;
SELECT ROUND(2.55555, 5); returns 3.00000 so, you can control the exactness by the second integer


### Date and Time

SELECT DATETIME('now'); returns the current date and time in UTC time zone
SELECT DATE('now'); returns the current date
SELECT TIME('now'); returns the current time
SELECT DATETIME('now', '+3 hours'); returns time 3 hours from  now

### Aggregates

SELECT Region, COUNT(*) AS Count
	FROM Country
	GROUP BY Region
	ORDER BY Count DESC, REGION
;
<!-- The above is counting countries and grouping them by region, then ordering them by Descending count, then region.

You can use the HAVING clause to further filter the returned results. HAVING works on aggregate data. It's the 'WHERE', but for aggregate data (aggregate data is data that has been put together with joins). WHERE is for non-aggregate data. -->


### TRANSACTIONS 
<!-- A transaction is a group of operations that are made into on unit (transaction). If any of the single operations fail, the entire group fails and the the DB is restored back to where it was before the transaction started. This can allow the writing to happen much faster because system doesn't have to confirm for each single insert that it has executed. -->

BEGIN TRANSACTION;
(some sql statement);
(some other sql statement);
END TRANSACTION;

<!-- (begin and end could vary slightly in syntax) -->


### TRIGGERS

<!-- Automatically performed when a specified database event occurs. Like forcing a table to be updated when a row is inserted or updated in another table. -->

CREATE TRIGGER newWidgetSale AFTER INSERT ON widgetSale
	BEGIN
		UPDATE widgetCustomer SET last_order_id = NEW.id WHERE widgetCustomer.id = NEW.customer_id;
	END
;

<!-- For the above: when there is an update on widgetSale table, it updates the last_order_id in the customer table and assigns it a value equal to the new widgetSale. -->

* Preventing automatic updates with a trigger
CREATE TRIGGER updateWidgetSale BEFORE UPDATE ON widgetSale
	BEGIN
		SELECT RAISE(ROLLBACK, 'cannot update table "widgetSale"') FROM widgetSale
			WHERE id = NEW.id AND reconciled = 1;
	END
;

<!-- This trigger fires before there's an update on the widgetSale table. If the 'reconciled' column = 1, then the transaction is rolled back and the 'cannot update...' message is raised. -->


* Making timestamps with triggers
<!-- **SIDENOTE**: dates and times are stored as text in SQL -->

CREATE TRIGGER stampSale AFTER INSERT ON widgetSale
	BEGIN
		UPDATE widgetSale SET stamp = DATETIME('now') WHERE id = NEW.id;
		(more sql ...)
		(more sql ...)
	END

### SUBSELECT
<!-- These are basically just nested select statements. Remember that the nested select is evaluated before the parent select. -->


SELECT * FROM album WHERE id IN (
	SELECT DISTINCT album_id FROM track WHERE duration <= 90
);


### VIEWS

CREATE VIEW trackView AS

	SELECT id, album_id, title, track_number, duration / 60 AS m, duration % 60 AS s FROM track;

<!-- then you could just call on trackView as a variable, essentially -->
SELECT * FROM trackView;

<!-- You can use DROP VIEW trackView to drop it just like a table. -->










