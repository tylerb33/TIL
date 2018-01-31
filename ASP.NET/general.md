**Benefits of ASP.NET MVC**

* Makes it easier to manage complexity by dividing an application into the model, the view, and the controller.

* Enables full control over the rendered HTML and provides a clean separation of concerns.

* Direct control over HTML also means better accessibility for implementing compliance with evolving Web standards.

* Facilitates adding more interactivity and responsiveness to existing apps.

* Provides better support for test-driven development (TDD).

* Works well for Web applications that are supported by large teams of developers and for Web designers who need a high degree of control over the application behavior.


**Razor Syntax Rules**

* Razor code blocks are enclosed in @{ ... }
* Inline expressions (variables and functions) start with @
* Code statements end with semicolon
* Variables are declared with the var keyword
* Strings are enclosed with quotation marks
* C# code is case sensitive
* C# files have the extension .cshtml


**Built-in Objects in ASP.NET**
The "DateTime" object is a typical built-in ASP.NET object, but objects can also be self-defined, a web page, a text box, a file, a database record, etc.

The ASP.NET ```DateTime``` object has a Now property (written as DateTime.Now), and the Now property has a Day property (written as DateTime.Now.Day). So you can call DateTime.Now.Hour to get the current hour in the Razor template.