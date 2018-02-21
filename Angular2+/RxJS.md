**Streams**
-Variables representing streams normally end in '$'



**Observables from events**
*Targeting Text Box with Observable*

const input = $('#input');
const inputStream$ = Rx.Observable.fromEvent(input, 'keyup');

inputStream$.subscribe(
	<!-- This first 'completed' code block is the only one required, but best practice to include all 3 -->
	function(e) {
		console.log(e.currentTarget.value);
	},
	function(err) {
		console.log(err);
	},
	function() {
		console.log('Completed');
	});


*Targeting Mouse Move*
const moveStream$ = Rx.Observable.fromEvent(document, 'mousemove');

moveStream$.subscribe(
	<!-- This first 'completed' code block is the only one required, but best practice to include all 3 -->
	function(e) {
		console.log(e.clientX);
	},
	function(err) {
		console.log(err);
	},
	function() {
		console.log('Completed');
	});




**Observables from arrays**
const numbers = [33, 44, 55, 111, 5];
const numbers$ = Rx.Observable.from(numbers);
numbers$.subscribe(
	v => {
		console.log(v);
	},
	err => {
		console.log(err);
	},
	complete => {
		console.log("Completed");
	}
});

const posts = [
	{title: 'Post One', body: 'This is the body'},
	{title: 'Post Two', body: 'This is the post two'},
	{title: 'Post Three', body: 'This is different'},
];

const posts$ = Rx.Observable.from(posts);

posts$.subscribe(
	v => {
		console.log(v);
	},
	err => {
		console.log(err);
	},
	complete => {
		console.log("Completed");
	}
});

*Create Observable from scratch*
const source$ = new Rx.Observable(observer => {
	observer.next('Hello World');
	observer.next('Another value');

	observer.error(new Error('Error: Something Wrong'));

	setTimeout(() => {
		observer.next('Yet another');
		observer.complete();
		}, 3000);
});

source$.subscribe(
	x => {
		console.log(x);
	},
	err => {
		console.log(err);
	},
	complete => {
		console.log('Completed')
}
});




**


****



****




****



****


****
****

****