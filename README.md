# Date Range Picker for Angular and Bootstrap
![Dependencies](https://david-dm.org/fragaria/angular-daterangepicker.png)

Angular.js directive for Dan Grossmans's [Bootstrap Datepicker](https://github.com/dangrossman/bootstrap-daterangepicker).

![Date Range Picker screenshot](http://i.imgur.com/zDjBqiS.png)

## Installation via Bower
The easiest way to install the picker is:
```
bower install angular-daterangepicker --save
```
## Manual installation
This directive depends on [Bootstrap Datepicker](https://github.com/dangrossman/bootstrap-daterangepicker), [Bootstrap](http://getbootstrap.com), [Moment.js](http://momentjs.com/) and [jQuery](http://jquery.com/).
Download dependencies above and then use [minified](js/angular-daterangepicker.min.js) or [normal](angular-daterangepicker.js) version.

## Basic usage
Assuming that bower installation directory is `bower_components`. In case of other installation directory, please update paths accordingly.

```
<script src="bower_components/jquery/jquery.js"></script>
<script src="bower_components/angular/angular.js"></script>
<script src="bower_components/momentjs/moment.js"></script>
<script src="bower_components/bootstrap-daterangepicker/daterangepicker.js"></script>
<script src="bower_components/angular-daterangepicker/js/angular-daterangepicker.js"></script>

<link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.css"/>
<link rel="stylesheet" href="bower_components/bootstrap-daterangepicker/daterangepicker-bs3.css"/>
```

Declare dependency:

```
App = angular.module('app', ['daterangepicker']);
```

Prepare model in your controller. The model **must** have `startDate` and `endDate` attributes: 

```
exampleApp.controller('TestCtrl', function ($scope) {
	$scope.date = {startDate: null, endDate: null};
}
```


Then in your HTML just add attribute `date-range-picker` to any input and bind it to model.

```
<div ng-controller="TestCtrl">
<input date-range-picker class="form-control date-picker" type="text" ng-model="date" />
</div>
```

See `example.html` for working demo.

## Advanced usage
Min and max value can be set via additional attributes:

```
<input date-range-picker class="form-control date-picker" type="text" ng-model="date" min="'2014-02-23'" max="'2015-02-25'"/>
```

The date picker can be later customized by passing `options` attribute.

<input date-range-picker class="form-control date-picker" type="text" ng-model="date" 
min="'2014-02-23'" max="'2015-02-25'" options="{separator: ":"}"/>

## Compatibility
Version > 0.1.1 requires [Bootstrap Datepicker](https://github.com/dangrossman/bootstrap-daterangepicker) 1.3.3 and newer.

Version 0.1.0 works with [Bootstrap Datepicker](https://github.com/dangrossman/bootstrap-daterangepicker) 1.3.2 and older. 

## Links
See [original documentation](https://github.com/dangrossman/bootstrap-daterangepicker).

