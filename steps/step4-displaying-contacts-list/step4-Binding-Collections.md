# Exercise: Display a contacts list

The aim of this exercise is to show how we can bind data collections that are a member property of a Data Source component.  

## Scenario

In order to render a list of contacts, we can use  a static list from `src/app/mockData/contact-data.ts`.  

```
export let CONTACT_DATA = [
                            {
                               id: 0,
                               name: 'Byron Thanopoulos',
                               email: 'byronth@gmail.com',
                               phone: '+44 1606 000000',
                               birthday: '1971-03-03',
                               website: 'icode.net',
                               image: '/app/assets//images/0.jpg',
                               address: {
                                 street: 'icode av. 1',
                                 zip: 'CW9 0PA',
                                 city: 'Manchester',
                                 country: 'UK'
                               }
                             },                              
  ...
```

Import that array, assign it a `contacts` property of `App` and use the `ngFor` directive to render a HTML list, based on that data, in `App`'s template.

## Steps

1. Import `CONTACT_DATA`
2. Create a property `contacts` in `App` and assign the collection.
3. Extend the existing static list in `App`'s view with `ngFor` and render a list item for each contact in the collection.
  Please note that directives are case sensitive.

### Additional resources and help

- [NgFor](https://angular.io/docs/ts/latest/api/common/NgFor-directive.html)
