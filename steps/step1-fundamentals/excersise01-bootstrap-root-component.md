# Angular Components and bootsrapping

Bootstrap an Angular2 application.

## Scenario

In `src/app/app.ts` you'll find the import statement:

```

import {Component} from 'angular2/core';

@Component({
  selector: 'app',
  templateUrl: 'app/app.html',

})
export class App {

}

```

And in `src/bootstrap.ts` you'll find:

```
import {bootstrap} from 'angular2/platform/browser';
import {App} from './app/app';
```

## Steps

1. We have created a class `App` and export it using `export`
2. We have Decorated `App` with `@Component()` decorator
3. We have Given the component an appropriate selector (`app`)
4. We have Defined a templateUrl (`app/app.html`) for the component
5. We used the given selector as tag in `index.html` i.e `<app>loading...</app>`
6. We have Bootstrapped i.e instruct angular to render the `App` in bootstrap.ts using the `bootstrap()`

### Setup

This project comes with a predefined build process. Once installed using

```
$ npm install
```
you can run the build process by executing

```
$ npm start
```

This will transpile the TypeScript source code and startup a webpack server on `localhost:8080`,
 where you can see the running app.





