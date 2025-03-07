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

