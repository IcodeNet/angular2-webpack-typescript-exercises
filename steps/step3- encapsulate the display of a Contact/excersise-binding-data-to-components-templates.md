# Exercise: Bind data to a component's template

Component properties sole purpose is to be used by the consumer of the component 
i.e. another component that uses our component (by adding it's selector element representation to its template)

## Scenario

In `src/app/models/contact.ts` you can find an interface definition of `Contact`.

```
interface Address {
  street: string;
  zip: string;
  city: string;
  country: string;
}

export interface Contact {
  id: number;
  name: string;
  email: string;
  phone: string;
  birthday: string;
  website: string;
  image: string;
  address: Address;
}
```

Import `Contact` and then create a `contact` member property of this type in `App` to render the data of a first contact in the component's 
template .

## Steps

1. Import `Contact`
2. Create a `contact` property of type `Contact` with the following object:

  ```
   {
    id: 0,
    name: 'Byron Thanopoulos',
    email: 'byronth@gmail.com',
    phone: '+44 1606 000000',
    birthday: '1971-03-03',
    website: 'icode.net',
    image: '/images/0.jpg',
    address: {
      street: 'icode av. 1',
      zip: 'CW9 0PA',
      city: 'Manchester',
      country: 'UK'
    }
  }
  ```

3. In order to Render the `contact` data use angular interpolation expressions and use for now the following template for the `Contact` template. 
 

  ```
  <ul class="collection">
    <li class="collection-item avatar">
      <img [src]="INSERT_CONTACT_IMAGE" alt="" class="circle">
      <span class="title">INSERT_CONTACT_NAME</span>
    </li>
  </ul>
  ```

Please read the background information on binding and the additional resources.

### Additional resources and help

- [Template Syntax - Property Binding](https://angular.io/docs/ts/latest/guide/template-syntax.html#!#property-binding)
