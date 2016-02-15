# Intro to AngularJS - Part 2

Let's continue exploring the built-in AngularJS directives.

So far we have seen:

* ng-app
* ng-controller
* ng-model
* ng-init
* ng-click

## Common AngularJS Directives (cont'd)

### Code-Along - Counter App with AngularJS

This code-along demonstrates the following AngularJS directives:

* ngApp
* ngController
* ngClick
* ngDisabled
* ngClass
* ngShow
* ngHide

[Codepen: Counter App](http://codepen.io/drmikeh/pen/bdrvRm?editors=111)

```html
<body ng-app="counterApp">
  <h1>Simple Counter with Controller</h1>
  <div ng-controller="counterCtrl as ctrl">
    <button ng-click="ctrl.increment()"
            ng-disabled="ctrl.isLimitExceeded()">Increment</button>
    <button ng-click="ctrl.decrement()"
            ng-disabled="ctrl.countIsZero()">Decrement</button>
    <button ng-click="ctrl.reset()">Reset</button>
    <h2 class="counter" ng-class="{red: ctrl.countIsZero()}">count: {{ ctrl.count }}</h2>
    <p ng-show="ctrl.isLimitExceeded()">You have exceeded your limit!</p>
    <p ng-hide="ctrl.isLimitExceeded()">You are doing great!</p>
  </div>
</body>
```

```css
button {
  font-size: 1.4em;
}

.counter {
  font-size: 1.5em;
}

.red {
  color: red;
  font-size: 2em;
}
```

```javascript
angular.module('counterApp', []);

angular.module('counterApp')
.controller('counterCtrl', function() {

  var limit = 10;

  this.reset = function() {
    this.count = 0;
  };

  this.reset();

  this.increment = function() {
    this.count = this.count + 1;
  };

  this.decrement = function() {
    this.count = this.count - 1;
  };

  this.isLimitExceeded = function() {
    return this.count >= limit;
  };

  this.countIsZero = function() {
    return this.count === 0;
  };
});
```

### Code-Along - Pets App with AngularJS

This code-along demonstrates:

* ngApp
* ngController
* ngModel
* ngDisabled
* ngRepeat and the orderBy filter
* ngRepeatStart
* ngRepeatEnd

[Codepen: Pets with ng-repeat](http://codepen.io/drmikeh/pen/RPbqMN)

```javascript
angular.module('myApp', []);
angular.module('myApp')
.controller('myController', function () {

  this.pets = [
    { name : 'Meisha',   species : 'dog', owner : 'Mike', vaccinated : true  },
    { name : 'Diesel',   species : 'dog', owner : 'Marc'  },
    { name : 'Snoopy',   species : 'dog', owner : 'Charlie'  },
    { name : 'Felix',    species : 'cat', owner : 'Susan'  }
  ];

  this.removeLastPet = function() {
    this.pets.pop();
  };
});
```

```html
<body ng-app="petsApp">
  <div ng-controller="petsCtrl as ctrl">
    <h2>Those crazy pets</h2>
    <ul>
      <li class="pet" ng-repeat="pet in ctrl.pets | orderBy : 'owner'">
        {{ pet.owner + " has a " +
        pet.species + " named " + pet.name }}
      </li>
    </ul>
    <button ng-click="ctrl.removeLastPet()">Remove Last</button>

    <h3 ng-repeat-start="pet in ctrl.pets">{{ pet.name }}</h3>
    <ul ng-repeat-end>
      <li>species: {{ pet.species }}</li>
      <li>owner: {{ pet.owner }}</li>
      <li>vaccinated: <input type="checkbox" ng-model="pet.vaccinated" ng-disabled="true"></li>
    </ul>
  </div>
</body>
```

```css
body {
  padding: 20px 40px;
  font-family: "Verdana";
}

h1 {
  text-align: center;
}

.pet {
  color: blue;
}
```


### ng-if


### ng-switch


### Filters

* currency
* uppercase
* orderBy


## AngularJS and the Module Pattern (closures)

Below are 2 approaches to avoiding global variables when declaring AngularJS modules. Either approach is valid, but the Module Pattern / closure approach is popular.

```javascript
// without closure - no global vars
angular.module('myApp', ['usersModule']);
angular.module('myApp')
.controller('todosCtrl', function(usersService) {
  this.users = usersService.users;
});

// Module Pattern with closure - no global vars
(function() {
  var app = angular.module('myApp', ['usersModule']);
  app.controller('todosCtrl', function(usersService) {
  this.users = usersService.users;
  });
})();
```
