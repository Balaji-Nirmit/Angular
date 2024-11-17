# Angular
<p>install angular CLI -- npm install -g @angular/cli</p>
<p>this installs globally</p>

<p>ng v :- this checks if angular is installed or not</p>
<p>ng new project_name  :- this creates a name</p>

<p>npm run start to start the program: this internally calls ng serve</p> 
<p>ng serve --o : this opens also</p>
<p>ng serve --port port_number : this open in the specified port</p>

![image](https://github.com/user-attachments/assets/3e6f1a5a-2d65-4b9e-a91d-22920fcb19a6)

<p>in package.json packages in <b>devDependency</b> helps to run locally so not included in build and packages in <b>Dependency</b> are build</p>

<p>in angular.json it is configuration or architecture file  which contains the first page index.html which can be changed here and main.ts file which is executed at first when an angular project is started</p>

<p>style.css file contain global css codes</p>
<p>tsconfig.json has configuration for typescript configuration</p>

<p>move to the project folder and to ass material UI then </p>
<p>ng add @angular/material</p>

<p>for tailwind css</p>
<p>npm install -D tailwindcss postcss autoprefixer</p>
<p>npx tailwindcss init -p         :---- This will create two files: tailwind.config.js and postcss.config.js.</p>

<h2>component</h2>
to create a coponent only component.ts file is needed
<p>to generate component :    ng g c component_name</p>
or
<p>ng generate component component_name</p>

![image](https://github.com/user-attachments/assets/05c369ef-2b02-49c9-a529-246508ce62eb)


here selector is its unique identifier
<p>standalone is true????</p>
<p>initially app.module.ts is there where all components were given which takes a lot time as it first loads all components first but since now they are standalone each component is loaded when triggered</p>


<h1>data binding</h1>

![image](https://github.com/user-attachments/assets/e04a5815-151e-4ce4-b9c7-d73ca22abaeb)


{{}} it is called interpolation which sets variable value in html 

<h2>property binding</h2>
properties are attributes

for this either use {{}} or [property_name]="variable_name" 


<h2>event binding</h2>
(event_name)="function_name()"

<h2>two way binding</h2>
using ngModel

![image](https://github.com/user-attachments/assets/34bb85ad-42ca-4c77-9960-23fb2867a04e)

using then the variable courseName will change as the data is typed in input box

<p>[(ngModel)]="variable_name"</p>

<h2>signal</h2>

varibale_name=signal(data);

<p>to access this {{variable_name()}}</p> 
called like methods


<p>to change the value of a signal</p>

this.singal_variable_name.set(data)

<h1>directive</h1>
<p>The Angular directive helps us to manipulate the DOM. You can change a DOM element’s appearance, behavior, or layout using the directives. They help you to extend HTML. The Angular directives are classified into three categories based on how they behave. </p> 
<ul><li>Component directive</li>
<li>Structural drective</li>
<li>Attribute Directive</li></ul>

<h2>Structural directive</h2>

<p>Structural directives can change the DOM layout by adding and removing DOM elements. All structural Directives are preceded by Asterix symbol</p>
<p>in angular 18 since stnadalone concept is there so to use any directive we have to import commonModule</p>

<h3>ngIf</h3>

![image](https://github.com/user-attachments/assets/22b75bba-7545-407e-913c-48abd558f9f5)

![image](https://github.com/user-attachments/assets/d4996a37-77a4-45c4-a811-2baf44d7d375)

![image](https://github.com/user-attachments/assets/51b99c37-aa89-4f3f-90d7-7b16755c9720)

<h3>ngIf else</h3>

![image](https://github.com/user-attachments/assets/121c67ce-4173-4327-95d4-fd012af5235e)

<h3>nfIf then else</h3>

![image](https://github.com/user-attachments/assets/71d3dc29-a584-481c-b8f9-a192d49e420e)

<p>Here, we have then clause followed by a template named thenBlock.
When the condition is true, the template thenBlock is rendered. If false, then the template elseBlock is rendered</p>

<h3>ngFor</h3>

![image](https://github.com/user-attachments/assets/ad31062e-24ac-4abe-bdd4-ad6b92fed1b5)

<h4>trackBy</h4>
<p>Angular uses the object identity to compare the elements in the collection to the DOM nodes. Hence when you add an item or remove an item, the Angular will track it and update only the modified items in the DOM. It does not render the entire list.

But this fails if we update the list from the backend server. That is because the retrieved objects cannot be compared with the existing objects in the list as the reference has changed. The Angular simply removes these elements from DOM and recreates the new elements from the new data. This has a huge performance implication.

Angular trackBy clause eliminates this problem, by telling angular how to identify similar elements. The Angular will use the value returned by the trackBy function to match the elements returned by the database and update the DOM Elements without recreating them.

We should always specify the primary key or unique key as the trackBy clause.</p>

![image](https://github.com/user-attachments/assets/5d64a783-5b0e-4eaf-afad-1b486cd60080)

<h2>Attribute directive</h2>
<p>An Attribute or style directive can change the appearance or behavior of an element.</p>
<h4>NgModel</h4>
<p>The ngModel directive is used the achieve the two-way data binding. We have covered ngModel directive in Data Binding in Angular Tutorial</p>
<h4>ngClass</h4>
<p>The ngClass is a directive that Angular uses to dynamically add or remove CSS classes to an HTML element based on certain conditions.</p>

![image](https://github.com/user-attachments/assets/aca31e1e-76d6-46ae-a290-7992795131ac)

<h5>NgClass with Array</h5>
<p>If the ngClass expression returns an array, Angular treats each array element as a CSS class.

The syntax is as follows.</p>

![image](https://github.com/user-attachments/assets/fcd156ce-be47-4c4a-8826-a164f1ef2105)

<h5>NgClass with Object</h5>
<p>You can also bind the ngClass to an object. The properties (keys) of the object will act as a class name. The properties must return a boolean value. If the return value is true, the class is applied. Else not.</p>

![image](https://github.com/user-attachments/assets/a38faea3-49c7-482f-95d2-f02f96dbbc91)

<h3>ngStyle</h3>

![image](https://github.com/user-attachments/assets/2f5dd0fa-dcf2-4a1b-8a13-0d39642e28e1)

![image](https://github.com/user-attachments/assets/98d7a039-5602-450a-9812-926b8d76c2d1)

![image](https://github.com/user-attachments/assets/59f5c5bf-c696-44d8-8636-dcafb8dc5233)


<h1>routing</h1>

app.routes.ts file is where routes are added
<p>Routing allows you to move from one part of the application to another part or one View to another View.

In Angular, Routing is handled by the Angular Router Module.</p>

<h6>angular router</h6>
<p>The Router is a separate module in Angular. It is in its own library package, @angular/router. The Angular Router provides the necessary service providers and directives for navigating through application views.

Using Angular Router you can

Navigate to a specific view by typing a URL in the address bar,
Pass optional parameters (query parameters) to the View,
Bind the clickable elements to the View and load the view when the user performs application tasks,
Handles back and forward buttons of the browser,
Allows you to load the view dynamically,
Protect the routes from unauthorized users using Route Guards</p>

![image](https://github.com/user-attachments/assets/b9922a52-a854-4e8b-8940-18f5f7bb051a)

<h3>components of angular router</h3>
<ul>
  <li><h4>Router</h4><p>An Angular Router is a service (Angular Router API) that enables navigation from one component to the next component as users perform application tasks like clicking on menus links, and buttons, or clicking on the back/forward button on the browser. We can access the router object and use its methods like navigate() or navigateByUrl(), to navigate to a route</p></li>
  
  <li><h4>Route</h4><p>Route tells the Angular Router which view to display when a user clicks a link or pastes a URL into the browser address bar. Every Route consists of a path and a component it is mapped to. The Router object parses and builds the final URL using the Route</p></li>
  <li><h4>Routes</h4><p>Routes is an array of Route objects our application supports</p></li>
  <li><h4>RouterOutlet</h4><p>The outerOutlet is a directive (<router-outlet>) that serves as a placeholder, where the Router should display the view</p></li>
  <li><h4>RouterLink</h4><p>The RouterLink is a directive that binds the HTML element to a Route. Clicking on the HTML element, which is bound to a RouterLink, will result in navigation to the Route. The RouterLink may contain parameters to be passed to the route’s component.</p></li>
  <li><h4>RouterLinkActive</h4><p>RouterLinkActive is a directive for adding or removing classes from an HTML element that is bound to a RouterLink. Using this directive, we can toggle CSS classes for active RouterLinks based on the current RouterState</p></li>
  <li><h4>ActivatedRoute</h4><p>The ActivatedRoute is an object that represents the currently activated route associated with the loaded Component.</p></li>
  <li><h4>RouterState</h4><p>The current state of the router includes a tree of the currently activated routes together with convenience methods for traversing the route tree.</p></li>
  <li><h4>RouterLink Parameters array</h4><p>The Parameters or arguments to the Route. It is an array that you can bind to RouterLink directive or pass it as an argument to the Router.navigate method.</p></li>
</ul>

![image](https://github.com/user-attachments/assets/46b23faa-706c-4895-9d68-04a9880666f5)

![image](https://github.com/user-attachments/assets/55876135-c33f-4f75-a3b6-05b3f39592e1)
