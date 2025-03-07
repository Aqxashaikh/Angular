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
