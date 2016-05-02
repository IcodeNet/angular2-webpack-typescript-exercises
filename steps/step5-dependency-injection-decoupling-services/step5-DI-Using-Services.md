# Exercise: DI - using a data Service

Instead of using static data Arrays tightly bound to our component we will use a service that provides the data we need and decouples our component responsibity of displaying the data from the retrieval. 

The aim of this step is to to see how to create services and how to inject them into an Angular application using providers.

## Scenario

`CONTACT_DATA` is an implementation detail we don't want to couple inside our application's component `App`. 

Instead we will create a service called `ContactsService` under `app\services\ContactsService.ts`:

The service will implement a `getContacts()` method that  will return the array of `CONTACT_DATA`. 

Use that new service by adding a provider to `bootstrap()` and injecting it into `App` component.

The responsibility of getting the data has now moved for the component to the service. 


## Steps

1. Create a `ContactsService`  
2. Import `CONTACT_DATA` in the service file
3. Create a method `getContacts()` which returns the array
4. Add `ContactsService` provider to `ContactsApp`'s `providers` property to make the service available in your app
5. Inject `ContactsService` in `App`
6. Use `ContactsService.getContacts()` to retreive the contacts data from the `App` component.

### Resources

 - [Dependency Injection (angular.io)](https://angular.io/docs/ts/latest/guide/dependency-injection.html)