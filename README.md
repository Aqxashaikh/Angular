# Angular
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script> # Dristributed Angular File System
AngularJS Extends HTML
AngularJS extends HTML with ng-directives.

The ng-app directive defines an AngularJS application.

The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.

The ng-bind directive binds application data to the HTML view.
-------------------------------------------------------------------
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>

<body>

<div ng-app="">
<p> hello,Aqsa Enter your text</P>
<p>Name: <input type="text" ng-model="name" placeholder="Enter name here"></p>
<H2>Hello {{name}}</H2>


</div>
</body>
</html>
-------------
<p ng-bind="name"></p>
<p>{{name}}</p>
-----------------------------
AngularJS modules define applications:

AngularJS Module
var app = angular.module('myApp', []);
------------------------------------------------------
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<p>Try to change the names.</p>

<div ng-app="myApp" ng-controller="myCtrl">

First Name: <input type="text" ng-model="firstName"><br>
Last Name: <input type="text" ng-model="lastName"><br>
<br>
Full Name: {{firstName + " " + lastName}}

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.firstName= "Aqsa";
    $scope.lastName= "Shaikh";
});
</script>

</body>
</html>
---------------
AngularJS Expressions
AngularJS expressions are written inside double braces: {{ expression }}.

AngularJS will "output" data exactly where the expression is written:

AngularJS Example
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
  <p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>
---------------------------------------------------
AngularJS Modules
An AngularJS module defines an application.

The module is a container for the different parts of an application.

The module is a container for the application controllers.

Controllers always belong to a module.

Creating a Module
A module is created by using the AngularJS function angular.module
----------------------------------------------
Modules and Controllers in Files
It is common in AngularJS applications to put the module and the controllers in JavaScript files.

In this example, "myApp.js" contains an application module definition, while "myCtrl.js" contains the controller:
html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script src="myApp.js"></script>
<script src="myCtrl.js"></script>

</body>
</html>
----------------------
myApp.js
var app = angular.module("myApp", []);
------------------------------
The [] parameter in the module definition can be used to define dependent modules.

Without the [] parameter, you are not creating a new module, but retrieving an existing one.

myCtrl.js
app.controller("myCtrl", function($scope) {
  $scope.firstName = "John";
  $scope.lastName= "Doe";
});

-------------------
<html></html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div data-ng-app="" data-ng-init="quantity=1;price=5">

<h2>Cost Calculator</h2>

Quantity: <input type="number" ng-model="quantity">
Price: <input type="number" ng-model="price">

<p><b>Total in dollar:</b> {{quantity * price}}</p>

</div>

</body>
</html>
------------------
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">
    <h1 ng-click="changeName()">{{firstname}}</h1>
</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.firstname = "Aqsa";
    $scope.changeName = function() {
        $scope.firstname = "Mansuri";
    }
});
</script>

<p>Click on the firstname to run the "changeName" function.</p>

<p>This example demonstrates how to use the controller to change model data.</p>

</body>
</html>



