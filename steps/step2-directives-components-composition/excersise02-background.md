#**Angular Components, Directives, dependencies and metadata Decorators**

An Angular2 component is just a javascript object that encapsulates data and behaviour.

in order to render something on a page angular needs to have some details/metadata about the Context.
    *  What is the tag name that component's code will augment
    *  what styles are available to the component to use
    *  what is the visual represenation of the component that will be rendered
    * ... and many more
    
    
 The Metadata will allow the framework to assemble together both the imperative and declarative instructions and render teh components template on the screen.
 
 Metadata are provided by means of decorator functions to the class components and its members. 
 
##Decorators
###A decorator function enables us to add metadata to a class and its members.

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
    
    
##The component selector

##Templates

##Embedded CSS

##View encapsulation options

##Summary

###Resources

- [ComponentFactory](https://angular.io/docs/ts/latest/api/core/ComponentFactory-interface.html)
