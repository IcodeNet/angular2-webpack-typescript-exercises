#**Angular Components, Directives, dependencies and metadata Decorators**

###An Angular2 component is just a javascript object that encapsulates data and behaviour. 

in order to render something on a page angular needs to have some details/metadata about the Context.
    *  What is the tag name that the component's code will augment ex. <app>loading</app>
    *  what styles are available to the component to use
    *  what is the visual represenation of the component when rendered i.e the components `template`
    * ... and more
    
    
 The Metadata will allow the Angular2 framework to assemble together both the imperative and declarative instructions 
 and render the component's template on the screen.
 
 
 Metadata are provided by means of decorator functions to the class components and its members. 
 
##Decorators
###A decorator function enables us to add metadata to a class and its members.

The purpose of the decorator is to allow the componnet to be `self describing`:

* How the component is tied to a tag in HTML, how is identified <contact></contact>
    * When we associate an angular component with a tag this will be called the host element 
* What are component inputs and outputs i.e. what data it needs in terms of input variables that are bound to input controls in its template and what events it will emit.
    * If we want our components to interact with the user we must use databinding in them
* How it draws it self and styles it self
* What are the dependencies and providers (services) that it depends uppon or uses. 
    * The template of a component will contain tags for subcomponents those components will be its dependencies. 

To apply a decorator to a class or one of the class members, 
we place it above the class or member that we want to decorate and invoke
it by prefixing with @ symbol as shown in the following example:

    @ClassDecorator()
        class Component {
            
            @MemberDecorator()
            member:type
        }
    
The `@Component` metadata decorator is one of several built in decorators that ships with
Angular 2 core. We use it specify the component's behavior and use.


An example of a component decorated is :

   
        import {Component} from 'angular2/core';


        @Component({
            selector: 'app-header-component',
            template: `
                    <div directive-class-selector >
                         <sub-component></sub-component>
                    </div>                 
            `,
            styleUrls: [],
            providers: [],
            directives: [DirectiveClassSelector, SubComponent],
            pipes: []
        })
        export class AppHeaderComponent {

            constructor() {}

        }
        
The minimum information that angular needs to render the abover component is:

    - the `selector`
    - the `template` or `templateUrl` 
    - and the dependencies i.e the subcomponents or directives (or services that it uses).      
 
###The view (template) of a component is just yet another DOM tree.     
    
##The component selector
    
    How a component is identified & used in either HTML or in other component templates si controlled by  the components selector that is passed on the Components decorator.
    
          @Component({
            selector: 'app-header-component',
            
            }
            
    In the above snippet we have declared that when inside another's components HTML or directly inside an HTML file we will use the `<app-header-component></app-header-component>`  

Angular will map the selector token `selector: 'app-header-component'` in this case to a custom element.

We can have the following selectors:

* `selector : 'app-header-component'`   usage : `<app-header-component></app-header-component>`

* `selector : '.app-header-component'`   usage : `<div class="app-header-component" ></div>`

* `selector : '[app-header-component]'`   usage : `<div app-header-component ></div>`

* `selector : 'div[app-header-component = include]'`   usage : `<div app-header-component = include ></div>`

* `selector : 'li:not[.selected]'`   usage : `<li></li><li class="selected" ></li>`

* `selector : 'app-header-component, .app-header-component, [app-header-component] '`   usage : `any of the above`


##Templates

##Embedded CSS

##View encapsulation options

##Summary

###Resources

- [ComponentFactory](https://angular.io/docs/ts/latest/api/core/ComponentFactory-interface.html)
