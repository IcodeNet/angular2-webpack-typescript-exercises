# Exercise: Composing the UI from Components and Directives

In the previous Step we found out how to bootstrap an Angular 2 applicastion by specifying the Root component.

Our `App` component was mapped by means of a `selector:'app'` to a named location in our HTML.

That location was where `<app>loading</app>` was placed in index.html. 
 
    <html>
        <head>
        </head>
    
        <body>

            <app>
            Loading...
            </app>
            
        
        </body>
    </html>



`<app>Loading...</app>` is the host element of our application.


In order to promote encapsulation and composition we have decided to split our application 
in to descrete parts of functionality.

## Background

Our `App` will have a header that will be shared among views.
In `src/app/components/app-header/app-header.ts` you can find the `AppHeaderComponent`.

Import that component and use it inside `App`'s template. Think that `<App>` is composed by different parts. One of them is `<AppHeaderComponent>`

Since `AppHeaderComponent` will be used by our `App` component so it needs to be added to the `directives`  
dependencies of it that is specified using the `App` components decorator.

## Tasks

1. Import `AppHeaderComponent`
2. Add it to `App` directives dependencies
3. Add `<app-header>` to `App` template view

