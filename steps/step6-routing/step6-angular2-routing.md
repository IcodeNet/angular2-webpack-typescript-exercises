# Exercise: Route to Contacts list Component

In this step we will start using angular Router

## Scenario

Currently in our root `App` component we use an `ngFor` to loop through an array of contacts and display them in the components template.

Obviously this is not the responsibility of `App` and it does not take advantage of the separation of concerns and single responsibility principles that Angular components allow.

So lets create a `ContactsListComponent` by extracting the current contacts list implementation into its own component.
So `App` will be what is supposed to be. A composition root.

We can create a new component `ContactsListComponent` in its own directory under `app/components\contacts-list-component'
 
## Tasks

1. Create a component `ContactsListComponent` under `app/components\contacts-list-component' and encapsulate the current contact list code currently in `App`
2. Import the new `ContactsListComponent` so it can be used in `App`
3. Import `ROUTER_PROVIDERS`, `ROUTER_DIRECTIVES` and `RouteConfig` from `angular2/router`
4. Add `ROUTER_PROVIDERS` to `App` providers.
5. Add `@RouteConfig()` decorator to `App` with a configuration where path `/` points to `ContactsListComponent` (look into RouteDefinition in Resources)
6. Add `ROUTER_DIRECTIVES` to `App`'s directive dependencies
7. Add `<router-outlet>` in `App`'s view to load and render components

Note: if nothing shows up remember to add `providers` and `directives` at the right place.

### Resources

- [RouteDefinition](https://angular.io/docs/ts/latest/api/router/RouteDefinition-interface.html)
- [ROUTER_PROVIDERS](https://angular.io/docs/ts/latest/api/router/ROUTER_PROVIDERS-let.html)
- [ROUTER_DIRECTIVES](https://angular.io/docs/ts/latest/api/router/ROUTER_DIRECTIVES-let.html)
- [RouterOutlet](https://angular.io/docs/ts/latest/api/router/RouterOutlet-directive.html)