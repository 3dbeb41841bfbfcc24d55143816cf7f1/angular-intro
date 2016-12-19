# Part 3 - Angular 1 Components

Let's look at our Simple Counter Angular App written as an Angular 1.5 Component.

Note that this code can be found at this [Codepen](http://codepen.io/drmikeh/pen/RovYRx?editors=1010#0).

## HTML

```html
<h1>Simple Counter with Controller</h1>
<section ng-app="counterApp">
  <simple-counter></simple-counter>
</section>
```

## CSS

```css
button {
  font-size: 1.4em;
}

.counter {
  font-size: 1.5em;
}

.blue {
  color: blue;
  font-size: 2em;
}

.red {
  color: red;
  font-size: 2em;
}
```

## JavaScript

```javascript
angular.module('counterApp', []);
angular.module('counterApp')
.component('simpleCounter', {
  template: `
<div>
    <button ng-click="$ctrl.increment()"
            ng-disabled="$ctrl.isLimitExceeded()">Increment</button>
    <button ng-click="$ctrl.decrement()"
            ng-disabled="$ctrl.countIsZero()">Decrement</button>
    <button ng-click="$ctrl.reset()">Reset</button>
    <h2 class="counter" 
        ng-class="{ red: $ctrl.countIsZero(),
                    blue: $ctrl.isLimitExceeded() }">count: {{ $ctrl.count }}</h2>
    <p ng-show="$ctrl.isLimitExceeded()">You have exceeded your limit!</p>
    <p ng-hide="$ctrl.isLimitExceeded()">You are doing great!</p>
  </div>
`,  
  controller: function() {
  
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
  }
});
```

## Bonus

Now try adding a 2nd counter:

```html
<h1>Simple Counter with Controller</h1>
<section ng-app="counterApp">
  <simple-counter></simple-counter>
  <simple-counter></simple-counter>
</section>
```

Nice :-)

> Components are great for reuse!!!
