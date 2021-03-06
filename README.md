![Alt text](/sample.PNG?raw=true)
# ng-smart-input
## Intro
Fancy performance grid capapable of: locking, re-ordering, show/hiding, template rendering... and a fancy indeterminate state


## Installing
* `npm install ng-smart-grid` 

## Usage
1. `<script type='text/javascript' src='ng-smart-grid/dist/app.min.js'></script>`
2. `angular.module('myApp', ['ng-smart-grid', 'ng-indeterminate'])`
3. provide a config object
4. or refer to sample app for basic setup

## Config Example
```javascript
this.gridConfig = {
	gridId: 'fancy-grid',
	preferences: [
		{id: 'id', title: 'Id', locked: true},
        {id: 'status', title: '<i class="fa fa-circle fa-fw" title="Status"></i>', displayFn: getStatusClass, locked: false},
        {id: 'name', title: 'Name', locked: false}
	]
};
```

## Data Example
```javascript
this.data = [
	{id: 1, name: 'Entity A', status: 'active'},
	{id: 2, name: 'Entity B', status: 'paused'}
	{id: 3, name: 'Entity C', status: 'active'}
];
```

## Known Limitations:
* locked columns area must not be larger than view port or all columns go over flown
* template is not compiled after injection. Compile at your own will
