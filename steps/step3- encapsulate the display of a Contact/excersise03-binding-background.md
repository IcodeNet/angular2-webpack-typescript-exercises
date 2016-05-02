
#Binding
Binding between two entities is usually provided by an object - the Binding object.
It glues together "two" properties- Data Source and Target, and keeps a channel of communication between them.

So when a `Binding` is declared/setup between an element (target) and a component ( data souce) - that element is called the binding's target.
 
The Bidnings Source will be the component that manages the template. All the parts are glued together by the framework.

Bindings in angular are declaratively setup.

In angular the binding's source is implicitly set to the component that owns the template that contains the target html element.

* So a `Source` Component will provide the data - Where the data are coming from.
* A Target HTML elemnt will receive the data   -Where the data is going.
* And a Binding object will Sync Between the two - what keeps the two synchronised.


so if we have the following component:

```

	@Component({
	selector: 'app',
	providers: [],
	templateUrl: `  <ul class="collection">
						<li class="collection-item avatar">
						<img [src]="contact.image" alt="" class="circle">
						<span class="title">{{ contact.name}}</span>
						</li>
					</ul>`,
	directives: [ ],
	pipes: []
	})
	export class App {
	
	private contact: Contact = {
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
								};
	
	}

```

The `App` component will be the source of a binding that is declared using the `{{ expression }}`.
The `App` component has been set as the implicit datasource (by Angular) that will be used for bindings inside the temlate.

The `<span>` element is the target of the binding that will receive the data from `App` and in particular will receive the value `contact.name` 
 