# Services, Providers and Factories

Services, providers and factories are still massively confusing in AngularJS, but in principle, a service and a factory are just shorthands to the more verbose provider declaration.

```
myModule.provider('aProvider', function() {

    // This is a PROVIDER

    this.$get = function() {

        // This is a FACTORY

        return new function() {

	    // This is a SERVICE

	    this.doSomething = function() {
	        return 'Hi!';
	    };
        };
    };
});

```

## Services and Factories

So, the factory above is equivalent to:

```
myModule.factory('aFactory', function() {

    return new function() {
        this.doSomething = function() {
	    return 'Hi!';
	};
    };
});
```

And, the service above is equivalent to:

```
myModule.service('aService', function() {

    this.doSomething = function() {
        return 'Hi!';
    };
};
```

But in reality, you can use both a service or a factory, just remember:
* For a service, the function you write will be `new`ed up: `new myService()`
* For a factory, the function that you write will be invoked: `myFactory()`

They're all singletons. Angular goes to this trouble with Dependency Injection to ensure that is true.

## Dependency Injection

If you wish to inject dependencies into your service or factory, remember that if you add these dependencies to the provider, they will not resolve. This is because providers are created at an earlier stage in Angular's lifecycle. It's their role to provide services!

But within a `provider` function, you can use `$inject` (or the more verbose `['myDependency], function(myDependency) {... }]` syntax:

```
myModule.provider('aProvider', function() {
    this.$get = function($document) {
        return new SuperService($document[0].body); // Just doing something with the injected dependency here...
    };
    this.$get.$inject = ['$document'];
});
```





