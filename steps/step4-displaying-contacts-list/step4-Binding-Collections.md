# Exercise: Display a contacts list

The aim of this exercise is to show how we can bind collections of data.
Those collections will be member properties of a Data Source component - part of the component's API.  

## Scenario

In order to render a list of contacts inside a components view, we can use as data source a static list from `src/app/mockData/contact-data.ts`.  

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

In our component we will consume the array by first Importing that array, 
then assign it to a `contacts` property of `App` component and finally 
use the `ngFor` directive to render a HTML list, based on that data, in `App`'s template.

## Steps

1. Import `CONTACT_DATA`
2. Create a property `contacts` in `App` and assign the collection.
3. Extend the existing static list in `App`'s view with `ngFor` and render a list item for each contact in the collection.
 
 NOTE: Please note that directives are case sensitive. So `ngfor` is not the same as `ngFor`

### Additional resources and help

- [NgFor](https://angular.io/docs/ts/latest/api/common/NgFor-directive.html)
