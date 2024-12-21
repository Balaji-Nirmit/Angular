![image](https://github.com/user-attachments/assets/953b2e84-2eb8-4da4-b99b-1ca6992ff8f1)# Angular
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


![image](https://github.com/user-attachments/assets/1e493d18-36ad-4e23-8b11-98d2817fecc6)

![image](https://github.com/user-attachments/assets/4c2f12ba-d2cc-4738-82d6-f0c182a536ae)

<h1>Control flow statements</h1>
@if, @if @elseif @else

![image](https://github.com/user-attachments/assets/1ffda969-6a43-460a-a04d-244c4a526d78)

![image](https://github.com/user-attachments/assets/35ec653b-b6f9-4434-a045-9b9e3f7b02fe)

![image](https://github.com/user-attachments/assets/fff174fe-d09c-496c-a3f3-176d9dff3f23)

@for

![image](https://github.com/user-attachments/assets/dc012548-e368-444e-83fa-8136e4f32539)

for structural dirctives we have to import common Module but when we use control flow statements then we don't have to import common module

<h1>pipe</h1>
<p>Angular Pipes takes data as input and formats or transform the data to display in the template. We use them to change the appearance of the data before presenting it to the user. The most common use case of pipes is displaying the dates in the correct format as per the user’s locale.</p>

<p>built-in pipes like currency pipe, date pipe, number pipe, percent pipe, decimal pipe, & slice pipe etc.</p>

![image](https://github.com/user-attachments/assets/755a031d-fe49-4782-a452-17e5ce37a8d4)

![image](https://github.com/user-attachments/assets/4cb79fd7-c6ba-4fef-bf2c-f26386e0fa25)

<p>for custom pipes view the official docs  <a href="https://angular.dev/api?type=pipe" target="_blank">click here</a></p>

to print objects on the dom use json pipe other wise [objects objects] this will be printed.

<h4>custom pipes</h4>
ng g p pipename  or ng generate pipe pipename

<p>pipes has transform function</p>

![image](https://github.com/user-attachments/assets/ca31266c-e0ee-4611-a7bf-14f361506785)


<h1>angular forms</h1>
<p>The Angular Forms module provides all the above services out of the box. It binds the form field to the Angular component class. It tracks changes made to the form fields so that we can respond accordingly. It also provides the built-in validators to validate the inputs. You can create your custom validator. It presents the validation errors to the user. Finally, it encapsulates all the input fields into an object structure when the user submits the form.

Angular takes two approaches to build the forms. One is <b>Template-driven</b> forms approach and another one is <b>Reactive forms</b> or model-driven forms approach</p>

<h2>Template driven form</h2>
<p>First, we build a simple HTML form using a few form elements. Then use the ngForm directive to convert them to Template-driven Form, which creates the top-level FormGroup control. Next, we use the ngModel directive to create the FormControl instance for each of the HTML form elements.</p>

<p>In Template Driven Forms we specify behaviors/validations using directives and attributes in our template and let it work behind the scenes. All things happen in Templates hence very little code is required in the component class. This is different from the reactive forms, where we define the logic and controls in the component class.</p>

![image](https://github.com/user-attachments/assets/74fbbfca-c9cf-4026-9d2e-798bb7bee051)

![image](https://github.com/user-attachments/assets/cbfc9807-493c-406c-8705-75bc861a3d49)

this code will give error since ngModel inside a form is not valid without a name tag.
<p>so name attribute is binded generally to objects fields which is binded to ngModel</p>

![image](https://github.com/user-attachments/assets/5c8334b0-baee-42f8-bb27-04408a0019f5)

![image](https://github.com/user-attachments/assets/df116ac1-9d55-4c88-b3fd-f6448b08ae50)

 now using a method called in html submit this

<h5>ngForm</h5>
<p>Once, we have a form with few form elements, the angular automatically converts it into a Template-driven form. This is done by the ngForm directive.

The ngForm directive is what makes the Angular template-driven forms work. But we do not need to do anything explicitly.

When we include FormsModule, the Angular is going to look out for any <form> tag in our HTML template. The ngForm directive automatically detects the <form> tag and automatically binds to it. You do not have to do anything on your part to invoke and bind the ngForm directive.</p>

![image](https://github.com/user-attachments/assets/bf6a566c-c8cc-4e11-abb7-dc73278eac1c)

![image](https://github.com/user-attachments/assets/5a8644bc-7be3-422d-b29e-3241762c4b12)

![image](https://github.com/user-attachments/assets/cc5261cf-3beb-4377-a240-4fd214e17f09)

<h5>validation in templte driven form</h5>

![image](https://github.com/user-attachments/assets/52686a75-c291-4971-89bd-dcaf2371c665)

![image](https://github.com/user-attachments/assets/14b67996-7ddb-432b-bc79-a9ed50794c7d)

![image](https://github.com/user-attachments/assets/5954687d-b3f9-4a8b-8796-87bd23cd9d7b)

<h2>reactive from</h2>
<p>Reactive forms ( also known as Model-driven forms) are one of the two ways to build Angular forms. In this tutorial, we will learn how to build a simple Example Reactive Form. To build reactive forms, first, we need to import ReactiveFormsModule. We then create the Form Model in component class using Form Group, Form Control & FormArrays. Next, we will create the HTML form template and bind it to the Form Model.</p>
<p>Reactive forms are forms where we define the structure of the form in the component class. i.e. we create the form model with Form Groups, Form Controls, and FormArrays. We also define the validation rules in the component class. Then, we bind it to the HTML form in the template. This is different from the template-driven forms, where we define the logic and controls in the HTML template.</p>

![image](https://github.com/user-attachments/assets/a6154153-5b12-405f-864e-fdff1d7e4bcc)

![image](https://github.com/user-attachments/assets/5237062f-099c-453c-be97-327bcf73fafd)

![image](https://github.com/user-attachments/assets/2817f954-2089-4d41-858c-bf30491cfdd0)

![image](https://github.com/user-attachments/assets/104b64fa-c0d7-44fb-89eb-c49e3d74c1ae)

![image](https://github.com/user-attachments/assets/4ca38ff2-089b-461a-98da-6e64299cb9e0)

![image](https://github.com/user-attachments/assets/67ac9e0a-186e-4337-b9ea-6b276bcb65b2)

![image](https://github.com/user-attachments/assets/4910280d-a31b-4170-acea-f3a8546c1e02)

![image](https://github.com/user-attachments/assets/1766ec9d-1c3b-410c-92f6-d6f2a6896781)

![image](https://github.com/user-attachments/assets/a017ad3e-70ca-4e91-b41a-aef2d5f3eed6)

![image](https://github.com/user-attachments/assets/bb659672-b0b5-40f5-967c-c9787a7c73fa)

![image](https://github.com/user-attachments/assets/6922dafb-88eb-4268-b030-843b2abeaeb3)

![image](https://github.com/user-attachments/assets/cc35eaf9-a62b-4a82-82c9-5a2f2cfe6dc9)





<h1>ngx mask</h1>

## Usage

```html
<input type="text" mask="<here goes your mask>" />
```

```html
<input type="text" [mask]="<here goes a reference to your component's mask property>" />
```

Also, you can use mask pipe.

```html
<span>{{phone | mask: '(000) 000-0000'}}</span>
```

You could path any valid config options, for example thousandSeparator and suffix

```html
<span>{{value | mask: 'separator': { thousandSeparator: ',', suffix: ' sm' } }}</span>
```

### Examples

| mask           | example        |
| -------------- | -------------- |
| 9999-99-99     | 2017-04-15     |
| 0\*.00         | 2017.22        |
| 000.000.000-99 | 048.457.987-98 |
| AAAA           | 0F6g           |
| SSSS           | asDF           |
| UUUU           | ASDF           |
| LLLL           | asdf           |

## Mask Options

You can define your custom options for all directives (as object in the mask module) or for each (as attributes for directive). If you override this parameter, you have to provide all the special characters (default one are not included).

### specialCharacters (string[ ])

We have next default characters:

| character |
| --------- |
| -         |
| /         |
| (         |
| )         |
| .         |
| :         |
| **space** |
| +         |
| ,         |
| @         |
| [         |
| ]         |
| "         |
| '         |

#### Usage

```html
<input type="text" [specialCharacters]="[ '[' ,']' , '\\' ]" mask="[00]\[000]" />
```

##### Then

```text
Input value: 789-874.98
Masked value: [78]\[987]
```

```typescript
patterns ({ [character: string]: { pattern: RegExp, optional?: boolean})
```

We have next default patterns:

| code  | meaning                                     |
| ----- | ------------------------------------------- |
| **0** | digits (like 0 to 9 numbers)                |
| **9** | digits (like 0 to 9 numbers), but optional  |
| **A** | letters (uppercase or lowercase) and digits |
| **S** | only letters (uppercase or lowercase)       |
| **U** | only letters uppercase                      |
| **L** | only letters lowercase                      |

##### Usage

```html
<input type="text" [patterns]="customPatterns" mask="(000-000)" />
```

and in your component

```typescript
public customPatterns = { '0': { pattern: new RegExp('\[a-zA-Z\]')} };
```

##### Then

```text
Input value: 789HelloWorld
Masked value: (Hel-loW)
```

### Custom pattern for this

You can define custom pattern and specify symbol to be rendered in input field.
Patterns may conflict with such letters as h, d, m, s, because we use these characters for dates.

```typescript
pattern = {
    B: {
        pattern: new RegExp('\\d'),
        symbol: 'X',
    },
};
```

### prefix (string)

You can add prefix to you masked value

#### Usage

```html
<input type="text" prefix="+7" mask="(000) 000 00 00" />
```

### suffix (string)

You can add suffix to you masked value

#### Usage

```html
<input type="text" suffix="$" mask="0000" />
```

### dropSpecialCharacters (boolean | string[])

You can choose if mask will drop special character in the model, or not, default value is `true`.

#### Usage

```html
<input type="text" [dropSpecialCharacters]="false" mask="000-000.00" />
```

##### Then

```text
Input value: 789-874.98
Model value: 789-874.98
```

### showMaskTyped (boolean)

You can choose if mask is shown while typing, or not, default value is `false`.

#### Usage

```html
<input mask="(000) 000-0000" prefix="+7" [showMaskTyped]="true" />
```

### allowNegativeNumbers (boolean)

You can choose if mask will allow the use of negative numbers. The default value is `false`.

#### Usage

```html
<input type="text" [allowNegativeNumbers]="true" mask="separator.2" />
```

##### Then

```text
Input value: -10,000.45
Model value: -10000.45
```

### placeHolderCharacter (string)

If the `showMaskTyped` parameter is enabled, this setting customizes the character used as placeholder. Default value is `_`.

#### Usage

```html
<input mask="(000) 000-0000" prefix="+7" [showMaskTyped]="true" placeHolderCharacter="*" />
```

### clearIfNotMatch (boolean)

You can choose clear the input if the input value **not match** the mask, default value is `false`.

### Pipe with mask expression and custom Pattern ([string, pattern])

You can pass array of expression and custom Pattern to pipe.

#### Usage

```html
<span>{{phone | mask: customMask}}</span>
```

and in your component

```typescript
customMask: [string, pattern];

pattern = {
    P: {
        pattern: new RegExp('\\d'),
    },
};

this.customMask = ['PPP-PPP', this.pattern];
```

### Repeat mask

You can pass into mask pattern with brackets.

#### Usage

```html
<input type="text" mask="A{4}" />
```

### Thousand separator

You can divide your input by thousands, by default will seperate with a space.

#### Usage

```html
<input type="text" mask="separator" />
```

For separate input with dots.

```html
<input type="text" mask="separator" thousandSeparator="." />
```

For using decimals enter `.` and how many decimals to the end of your input to `separator` mask.

```html
<input type="text" mask="separator.2" />
```

```text
Input value: 1234.56
Masked value: 1 234.56

Input value: 1234,56
Masked value: 1.234,56

Input value: 1234.56
Masked value: 1,234.56
```

```html
<input type="text" mask="separator.2" thousandSeparator="." />
<input type="text" mask="separator.2" thousandSeparator="," />
<input type="text" mask="separator.0" thousandSeparator="." />
<input type="text" mask="separator.0" thousandSeparator="," />
```

For limiting decimal precision add `.` and the precision you want to limit too on the input. **2** is useful for currency. **0** will prevent decimals completely.

```text
Input value: 1234,56
Masked value: 1.234,56

Input value: 1234.56
Masked value: 1,234.56

Input value: 1234,56
Masked value: 1.234

Input value: 1234.56
Masked value: 1,234
```

```html
<input type="text" mask="separator.2" [leadZero]="true" />
```

To add zeros to the model at the end

```text
Input value: 12
Masked value: 12.00

Input value: 12.1
Masked value: 12.10
```

```html
<input type="text" mask="separator.2" separatorLimit="1000" />
```

For limiting the number of digits before the decimal point you can set `separatorLimit` value to _10_, _100_, _1000_ etc.

```text
Input value: 12345678,56
Masked value: 1.234,56
```

### Time validation

You can validate your input as 24 hour format.

#### Usage

```html
<input type="text" mask="Hh:m0:s0" />
```

### Date validation

You can validate your date.

#### Usage

```html
<input type="text" mask="d0/M0/0000" />
```

### leadZeroDateTime (boolean)

If the `leadZeroDateTime` parameter is `true`, skipped symbols of date or time will be replaced by `0`. Default value is `false`.

#### Usage

```html
<input type="text" mask="d0/M0/0000" [leadZeroDateTime]="true" />
```

```text
Input value: 422020
Masked value: 04/02/2020
```

```html
<input type="text" mask="Hh:m0:s0" [leadZeroDateTime]="true" />
```

```text
Input value: 777
Masked value: 07:07:07
```

### Percent validation

You can validate your input for percents.

#### Usage

```html
<input type="text" mask="percent" suffix="%" />
```

### FormControl validation

You can validate your `formControl`, default value is `true`.

#### Usage

```html
<input type="text" mask="00 00" [validation]="true" />
```

### Secure input

You can hide symbols in input field and get the actual value in `formcontrol`.

#### Usage

```html
<input placeholder="Secure input" [hiddenInput]="true" mask="XXX/X0/0000" />
```

### IP valid mask

#### Usage

```html
<input mask="IP" />
```

### CPF_CNPJ valid mask

#### Usage

```html
<input mask="CPF_CNPJ" />
```

### Allow few mask in one expression

#### Usage

You can pass into mask pattern with `||`.

```html
<input mask="000.000.000-00||00.000.000/0000-00" />
```

```html
<input mask="(00) 0000-0000||(00) 0 0000-0000" />
```

```html
<input mask="00||SS" />
```

### Function maskFilled

#### Usage

```html
<input mask="0000" (maskFilled)="maskFilled()" />
```


<h1>GET API using HttpClient</h1>

<p>The HttpClient is a separate model in Angular and is available under the @angular/common/http package. The following steps show you how to use the HttpClient in an Angular app.</p>

![image](https://github.com/user-attachments/assets/398cb2d0-42ad-418c-9af8-d4c8a594f75f)

![image](https://github.com/user-attachments/assets/1f55de6b-328b-4416-a932-09b20b5335fa)

In app.config.ts we need to provide httpclient in providers array
<b>provideHttpClient()</b>

<p>after this import in any component required and dependency injection</p>

httpClient has 4 methods 
GET, POST, PUT, DELETE

<h2>GET request</h2>
<p>To make HTTP Get request, we need to make use of the HttpClientModule, which is part of the package @angular/common/http. Open the app.module.ts and import it. Also, import the FormsModule</p>

![image](https://github.com/user-attachments/assets/8f28f65c-9991-4f3d-a9c9-06b11c9e4db9)

![image](https://github.com/user-attachments/assets/af696206-6fe6-43ed-8d0c-66ffde88e5e9)

but this is deprecated and will learn he new way in obesrvables.

<h2>POST request</h2>

![image](https://github.com/user-attachments/assets/94bb606a-56df-424a-9263-18d8ef5d940e)

![image](https://github.com/user-attachments/assets/3c8437e8-ac86-463f-bb93-5226674c8bed)


<h2>PUT and DELETE request</h2>

When we update a form we need to patch it and then update it.

![image](https://github.com/user-attachments/assets/fa8aa0f5-893a-4533-9bfc-7edb6cc9285e)


<h1>Services</h1>
<p>Service is a piece of reusable code with a focused purpose. A code that you will use in many components across your application

Our components need to access the data. You can write data access code in each component, but that is very inefficient and breaks the rule of single responsibility. The Component must focus on presenting data to the user. The task of getting data from the back-end server must be delegated to some other class. We call such a class a Service class. Because it provides the service of providing data to every component that needs it.</p>

![image](https://github.com/user-attachments/assets/c0e09c18-0c4b-476f-b530-bd05a807c839)

<strong>ng g s service_name</strong>
<strong>ng generate service service_name</strong>


![image](https://github.com/user-attachments/assets/5e870e23-579e-42b3-be93-bf22decd81ec)

it has injectable decorator

![image](https://github.com/user-attachments/assets/8da41e28-7032-4df2-991c-58a83e7b32bd)

there are two ways for injecting services into component 

<ul><li>using inject</li><li>dependency injection</li></ul>

![image](https://github.com/user-attachments/assets/4f2791ac-c88c-4a1a-bf98-12ed95ebe7d4)

in constructor it is called dpendency injection


<h1>Input and Output Decorators</h1>
<p>Input decorator marks the property as the input property. I.e it can receive data from the parent component. The parent component uses the property binding to bind it to a component property. Whenever the value in the parent component changes angular updates the value in the child component.</p>

![image](https://github.com/user-attachments/assets/0a124a04-e454-4e34-940a-ccb38de4e608)

<p>The parent component supplies the customer object using the property binding syntax. We add a square bracket around the customer property. Assign template expression (selectedCustomer) to it, which is a property in the parent component.</p>

![image](https://github.com/user-attachments/assets/79792fec-43e0-4b47-9990-3425143ac143)

<p>Output decorates the property as the output property. We initialize it as an EventEmitter. The child component raises the event and passes the data as the argument to the event. The parent component listens to events using event binding and reads the data.</p>

![image](https://github.com/user-attachments/assets/6e7e171d-fd73-4914-86fe-d8a235a8929e)

![image](https://github.com/user-attachments/assets/6c7c489b-bc42-4337-84ec-bdeb07326477)

![image](https://github.com/user-attachments/assets/94efdf0b-acac-4356-9cd7-762d12f545c9)

easy way:-
<p>in child component</p>

![image](https://github.com/user-attachments/assets/bc4df662-96ca-450a-83ac-99b33895b070)

![image](https://github.com/user-attachments/assets/b9f625c5-1523-4615-a634-da987e63b049)


<p>in parent component </p>

![image](https://github.com/user-attachments/assets/efb5fb3f-2186-440f-b2c7-8c01d5aa5d61)

the method getData is in parent component which will receive the data from child


<h1>Life Cycle Hooks</h1>

<p>Lifecycle hooks are Angular methods that are executed at certain points during a component's lifecycle. These methods allow you to tap into the Angular component lifecycle and apply custom logic or operations at specified points in time.</p>

![image](https://github.com/user-attachments/assets/52a089b6-582c-4df7-8f04-def79fb0b23b)

very first the constructor is called

# Angular Lifecycle Hooks

Angular provides several lifecycle hooks that allow you to run custom logic at different stages of a component's life cycle. Below are the key lifecycle hooks in Angular:

## `ngOnChanges`

The `ngOnChanges` lifecycle hook is invoked whenever there are changes in the input properties of a component. It is called before `ngOnInit` and responds when data-bound input properties are set or reset. This method receives a `SimpleChanges` object containing the previous and current values of the input properties.

- **Triggered when**: Data-bound input properties change.
- **Use case**: To respond to changes in input properties.
- **Invoked before**: `ngOnInit`.

---

## `ngOnInit`

The `ngOnInit` lifecycle hook is invoked once the component is initialized, after Angular has set the input properties. It is invoked after `ngOnChanges` and is used for component initialization logic.

- **Triggered when**: Component is initialized.
- **Use case**: Initialize data or perform setup logic for the component.
- **Invoked after**: `ngOnChanges` (if input properties exist).

---

## `ngDoCheck`

The `ngDoCheck` lifecycle hook is invoked during every change detection cycle. It allows you to detect and act upon changes that Angular may not automatically detect.

- **Triggered when**: During every change detection cycle, even without input property changes.
- **Use case**: To implement custom change detection logic.
- **Invoked after**: `ngOnChanges` and `ngOnInit`.

---

## `ngAfterContentInit`

The `ngAfterContentInit` lifecycle hook is called once after Angular has fully initialized the content projected into the component (via `ng-content`). This hook is invoked only once.

- **Triggered when**: Content has been projected into the component's view.
- **Use case**: Initialize or process projected content.
- **Invoked after**: `ngDoCheck` and before `ngAfterContentChecked`.

---

## `ngAfterContentChecked`

The `ngAfterContentChecked` lifecycle hook is invoked after the content projection has been checked for changes. This hook runs after every change detection cycle.

- **Triggered when**: The projected content is checked for changes.
- **Use case**: Respond to changes in projected content.
- **Invoked after**: `ngDoCheck`, `ngAfterContentInit`, and every change detection cycle.

---

## `ngAfterViewInit`

The `ngAfterViewInit` lifecycle hook is called once after the view and its child views have been initialized. It is invoked only once in the component lifecycle.

- **Triggered when**: The component’s view and child views are initialized.
- **Use case**: To initialize or access the component’s view and child components.
- **Invoked after**: `ngAfterContentChecked`.

---

## `ngAfterViewChecked`

The `ngAfterViewChecked` lifecycle hook is invoked after Angular checks the view and child views of the component for changes. It is called after every change detection cycle.

- **Triggered when**: The component’s view and child views are checked for changes.
- **Use case**: Respond to changes in the view.
- **Invoked after**: `ngAfterViewInit` and after each change detection cycle.

---

## `ngOnDestroy`

The `ngOnDestroy` lifecycle hook is called when Angular is about to destroy the component. This is a good place to clean up resources like unsubscribing from observables or removing event listeners to avoid memory leaks.

- **Triggered when**: The component is destroyed.
- **Use case**: Clean up resources like subscriptions, event listeners, or custom cleanup logic.
- **Invoked before**: Component is removed from the DOM.

---

### Summary

| Lifecycle Hook           | Triggered When                                              | Invoked Before          | Invoked After          |
|--------------------------|-------------------------------------------------------------|-------------------------|------------------------|
| `ngOnChanges`             | When input properties change                               | -                       | `ngOnInit`             |
| `ngOnInit`                | After component initialization and input properties are set | `ngOnChanges`           | `ngDoCheck`            |
| `ngDoCheck`               | During every change detection cycle                         | `ngOnInit`              | `ngAfterContentInit`   |
| `ngAfterContentInit`      | After content is projected into the component               | `ngDoCheck`             | `ngAfterContentChecked`|
| `ngAfterContentChecked`   | After content checking completes                            | `ngAfterContentInit`    | `ngAfterViewInit`      |
| `ngAfterViewInit`         | After view and child views are initialized                  | `ngAfterContentChecked` | `ngAfterViewChecked`   |
| `ngAfterViewChecked`      | After view and child views are checked                      | `ngAfterViewInit`       | -                      |
| `ngOnDestroy`             | When component is about to be destroyed                     | -                       | -                      |

These hooks help manage the lifecycle of an Angular component, from initialization to destruction, providing opportunities for you to insert custom logic at each stage.


### Ng-Template and TemplateRef

<p>The <ng-template> is an Angular element, which contains the template. A template is an HTML snippet. The template does not render itself on DOM.</p>

![image](https://github.com/user-attachments/assets/175a4fad-dee7-48a0-bbc2-b8b8bf6a1d79)

![image](https://github.com/user-attachments/assets/4fefd88b-2fd0-4e3f-9a47-6c77ce4538ad)

![image](https://github.com/user-attachments/assets/d994e668-e40d-45c2-89b3-de1fed200de9)

![image](https://github.com/user-attachments/assets/067e032e-d2a7-40e1-85f3-d1621853c9f3)

<h2>ngTemplateOutlet</h2>
<p>The ngTemplateOutlet, is a structural directive, which renders the template.

To use this directive, first, we need to create the template and assign it to a template reference variable (sayHelloTemplate in the following template).</p>

![image](https://github.com/user-attachments/assets/3673adda-27a9-480c-bfff-e305d2ca1e38)

<p>We use the ngTemplateOutlet in the DOM, where we want to render the template.</p>
<p>The following code assigns the Template variable sayHelloTemplate to the ngTemplateOutlet directive using the Property Binding.</p>

![image](https://github.com/user-attachments/assets/1a3df7d0-d78e-47c2-9104-a5b75e69d591)

<p>The content inside the ngTemplateOutlet directive is not displayed. It replaces it with content it gets from the sayHelloTemplate.

The ngTemplateOutlet is a very powerful directive. You can use it render templates, pass data to the template, pass the template to child components, etc.</p>

<h2>TemplateRef & ViewContainerRef</h2>

<p>TemplateRef is a class and the way to reference the ng-template in the component or directive class. Using the TemplateRef we can manipulate the template from component code.

Remember ng-template is a bunch of HTML tags enclosed in a HTML element <ng-template></p>

![image](https://github.com/user-attachments/assets/cfa35f88-f59c-4e5c-9d33-43c1eeaeb0a2)

<p>To access the above ng-template in the component or directive, first, we need to assign a template reference variable. #sayHelloTemplate is that variable in the code below.</p>

![image](https://github.com/user-attachments/assets/b456f650-e0cd-4890-8b2b-7ba8a47a6bae)

<p>Now, we can use the ViewChild query to inject the sayHelloTemplate into our component as an instance of the class TemplateRef.</p>

![image](https://github.com/user-attachments/assets/6d2414a4-a4f1-476a-9f61-438fb86b99fd)

Now, we need to tell Angular where to render it. The way to do is to use the ViewContainerRef.

![image](https://github.com/user-attachments/assets/fa738099-bd92-4be8-8932-0f30be45e771)

![image](https://github.com/user-attachments/assets/b5984798-9c0d-45b5-8665-2970ced1f233)

![image](https://github.com/user-attachments/assets/250896ef-4e78-4db3-860b-2170ae3078a6)



<h1>ng-container</h1>

<p>ng-container allows us to create a division or section in a template without introducing a new HTML element. The ng-container does not render in the DOM, but content inside it is rendered. ng-container is not a directive, component, class, or interface, but just a syntax element.</p>

limitation of structural directive is that one element can't have more than one structural directive.



<h1>View Child</h1>

The ViewChild query returns the first matching element from the DOM and updates the component variable on which we apply it.

![image](https://github.com/user-attachments/assets/76a6074a-ff96-4629-b9a1-40360dc7f4f3)

viewchild is a decorator

![image](https://github.com/user-attachments/assets/add43579-0cb5-487c-91f7-9b90257643d2)

we mostly use afterViewInit for viewchilds

![image](https://github.com/user-attachments/assets/85d9d893-e94e-4a7f-93f5-dbabc9a1e03e)

we can also create a reference of a reusable component

![image](https://github.com/user-attachments/assets/f3f8c860-759e-4965-9657-09c814978864)

 ![image](https://github.com/user-attachments/assets/cdf4d254-0259-4b32-abdd-5334293e49cd)

it is needed to call the reusable component in html also otherwise undefined response will come. 

![image](https://github.com/user-attachments/assets/afb3eb45-8e25-4118-818a-78e890c1547b)

so whenever using external libraries like of graphs, etc use viewchild.


# decorators

<p>An Angular Decorator is a function, using which we attach metadata to a class declaration, method, accessor, property, or parameter.

We apply the decorator using the form @expression, where expression is the name of the decorator.</p>
<p>The decorator is a Typescript feature and it is still not part of the Javascript. It is still in the Proposal stage.</p>

<p>Angular uses the Decorators to Provide metadata to the class, method, or property.

For example, the AppComponent must know where to find its template. We do that by using the templateUrl parameter of the @Component directive. The @Component decorator also accepts the values for styleUrls, encapsulation, changeDetection, etc, which Angular uses to configure the component.</p>

there are
<ul>
  <li>class decorator</li>
  <li>property decorator</li>
  <li>method decorator</li>
  <li>parameter decorator</li>
</ul>

![image](https://github.com/user-attachments/assets/2588c453-3188-4202-a2ec-65515753fac9)


# ROUTE gaurds

<p>We use the Angular Guards to control whether users can navigate to or away from the current route.</p>
<p>One of the common scenarios where we use Route guards is authentication. We want our app to stop the unauthorized user from accessing the protected route. We achieve this by using the CanActivate guard, which angular invokes when the user tries to navigate into the protected route. Then we hook into the CanActivate guard and use the authentication service to check whether the user is authorized to use the route or not. If he is not authenticated, then we can redirect the user to the login page.</p>

![image](https://github.com/user-attachments/assets/bad592af-0a6e-4042-befa-c67a30ab5bfd)


## CanActivate
The Angular CanActivate guard decides if a route can be activated ( or the component gets rendered). We use this guard when we want to check on some condition, before activating the component or showing it to the user. This allows us to cancel the navigation.

Use cases
<li>Checking if a user has logged in</li>
<li>Checking if a user has permission</li>
One of the use cases of this guard is to check if the user has logged in to the system. If the user has not logged in, then the guard can redirect him to the login page.

## CanDeactivate
This Angular Guard decides if the user can leave the component (navigate away from the current route). This route is useful when the user might have some pending changes, which is not yet saved. The CanDeactivate route allows us to ask for user confirmation before leaving the component.  You might ask the user if it’s OK to discard pending changes rather than save them.

## Resolve
This guard delays the activation of the route until some tasks are complete. You can use the guard to pre-fetch the data from the backend API before activating the route.

## CanLoad
The CanLoad Guard prevents the loading of the Lazy Loaded Module. We generally use this guard when we do not want to unauthorized users to be able even to see the source code of the module.

This guard works similarly to CanActivate guard with one difference. The CanActivate guard prevents a particular route from being accessed. The CanLoad prevents the entire lazy-loaded module from being downloaded, protecting all the routes within that module.

## CanActivateChild
CanActivateChild guard determines whether a child route can be activated. This guard is very similar to CanActivateGuard. We apply this guard to the parent route. The Angular invokes this guard whenever the user tries to navigate to any of its child routes. This allows us to check some conditions and decide whether to proceed with the navigation or cancel it.


### steps 

first  ng g g guard_file_name
 then asked for gaurd:- choose the gaurd

 ![image](https://github.com/user-attachments/assets/08cb7b2a-d5bb-4ec3-b29b-2cd2e7544adc)

![image](https://github.com/user-attachments/assets/25ee418b-e6cc-450a-9aa3-5a1164621c0f)

![image](https://github.com/user-attachments/assets/c993c336-98a7-46f0-a1d8-573a0fb84a6a)

now we need to write the logic for the gaurd function in the gaurd file--
example:-

![image](https://github.com/user-attachments/assets/72f99473-cbae-4e35-934c-e019027731f3)

# constant file

it is a normal .ts file.

![image](https://github.com/user-attachments/assets/a7189c90-3bd3-48e6-8e44-b066be409fb9)


# class and interface

A class is a blueprint for creating objects, defining the properties and methods that the object can have. In Angular, classes are used for:

<li>Component Classes: Every Angular component is a class that defines the component’s logic, properties, and methods.</li>
<li>Service Classes: Services in Angular are often implemented as classes and can be injected into components or other services to share logic across the application.</li>
<li>Directive Classes: Custom directives are also written as classes in Angular.</li>
<li>Model Classes: Classes can be used to define the data structure (model) for specific types of data that will be used in your app.</li>


<p>An interface in TypeScript is a way to define the structure or shape of an object, but unlike classes, it cannot be instantiated. Interfaces define the required properties and methods that an object must have.

In Angular, interfaces are often used to define the structure of data, such as models or responses from an API. They ensure that objects conform to a specific structure, which improves type safety.</p>

![image](https://github.com/user-attachments/assets/1651c659-b98a-41b4-9b92-8e968f61b895)

# signal

replacement of observable
<p>In Angular, signals are a reactive mechanism used to handle state and data flow. Signals are a relatively new feature in Angular (introduced in Angular 16) and they provide a way to manage and react to changes in state within an application, similar to reactive programming concepts seen in libraries like RxJS.</p>

<p>Signals are objects that hold values and notify consumers when the value changes. A signal is created by using the signal() function, and its value can be updated, observed, and reacted to directly.</p>

<li>we call signal as a method</li>

![image](https://github.com/user-attachments/assets/2f943716-a0ee-4979-8f2b-226a4ccaa3f9)

![image](https://github.com/user-attachments/assets/f1cdd389-902f-4a1e-85c2-746db1e2099b)

![image](https://github.com/user-attachments/assets/485e8fce-a2c2-47a3-99cb-e983b0736669)

![image](https://github.com/user-attachments/assets/e1fe479b-6dd5-449b-947b-57e29c7c4a12)

here the set method is used to change the value 

<p>how signal is different is that it doesn't need zone.js for change detection</p>

#### computed

<p>The computed() function in Angular provides a way to automatically derive and update values based on other signals, similar to the concept of computed properties in frameworks like Vue.js or Svelte.</p>

![image](https://github.com/user-attachments/assets/a70eb3e9-9564-4fec-b7e4-c081f442edb7)

whenever firstname <b>or</b> lastname changes fullname would be computed.

![image](https://github.com/user-attachments/assets/16900dee-cc53-420b-95c8-8179dab57e0a)

if curly brackets are used then return statement is used.



# observable using RxJs

## data stream

<p>A data stream is the data that arrives over some time. The stream of data can be anything. Like variables, user inputs, properties, caches, data structures, and even failures, etc

Consider the example of a sequence of x and y positions of mouse click events. Assume that the user has clicked on the locations (12, 15), (10, 12), (15, 20), and (17, 15) in that order.
The following diagram shows how the values arrive over a period of time. As you can see, the stream emits the values as they happen, i.e., asynchronously.</p>

![image](https://github.com/user-attachments/assets/3bef1e75-8c69-43fc-87bd-7e3aafd121e8)

![image](https://github.com/user-attachments/assets/5634604e-19eb-42fb-afc1-276c946bcce6)

## RxJs

<p>The RxJS (Reactive Extensions Library for JavaScript) is a Javascript library that allows us to work with asynchronous data streams.</p>

![image](https://github.com/user-attachments/assets/a9dda645-7e01-4459-a4f6-f1478a895e8f)

## observable

<p>Observable is a function that converts the ordinary data stream into an observable one. You can think of Observable as a wrapper around the ordinary data stream.

An observable stream or simple Observable emits the value from the stream asynchronously. It emits the complete signals when the stream completes or an error signal if the stream errors out.

Observables are declarative. You define an observable function just like any other variable. The observable starts to emit values only when someone subscribes to it.</p>

<p><strong>Generally we store observable datas in a variable ending with a dollar sign example:- accountNumberData$ </strong></p>
it is just a standard not necessary but should be followed.

![image](https://github.com/user-attachments/assets/3c9671aa-3e59-4a23-bafd-cb2455c6e6ee)

![image](https://github.com/user-attachments/assets/9e79b0c9-13ad-4021-8258-ebdbf146ea0b)

![image](https://github.com/user-attachments/assets/2faa6614-49ba-4ba2-825b-387b3c27320c)

### RxJS subject

<p>RxJS Subjects are a powerful way to handle and manage streams of data. A Subject is both an Observable and an Observer: it can emit values like an Observable and can also be subscribed to, making it a central part of reactive programming. Subjects are particularly useful in scenarios where you need to multicast data to multiple observers or components.</p>

<p>A Subject is a special kind of Observable that allows values to be multicast to many Observers. Unlike a regular Observable, which can only be subscribed to once, a Subject allows multiple subscribers and pushes the same values to all subscribers.</p>

![image](https://github.com/user-attachments/assets/1499c92e-1048-4194-84ef-d52488c640f7)

 ![image](https://github.com/user-attachments/assets/be8a4624-41c5-49dd-9953-6cdae3a84ae1)

next method to send data

![image](https://github.com/user-attachments/assets/f1ad8c29-a286-48bb-bccf-db7fba1fc768)

subscribe to get 


![image](https://github.com/user-attachments/assets/c992e006-dfa6-4b54-8d03-968b76709b3a)

![image](https://github.com/user-attachments/assets/abddb9d1-62bf-494a-b933-7e21aab2dd50)

![image](https://github.com/user-attachments/assets/3fa9bfed-b935-4534-b355-9840c48db8ea)

![image](https://github.com/user-attachments/assets/2740b13d-4486-4db3-b8d0-f92430e7bf19)

```typescript
import { Observable } from 'rxjs';

const observable = new Observable<string>((observer) => {
  observer.next('Hello');
  observer.next('World');
  observer.complete();  // Mark the observable as complete
});

observable.subscribe({
  next: (value) => console.log(value),  // Handle emitted values
  complete: () => console.log('Completed!')  // Handle completion
});
```

![image](https://github.com/user-attachments/assets/0a2785e5-5a1b-4e0c-afb0-46972ae65893)

```typescript
const observer = {
  next: (value: string) => console.log(`Received: ${value}`),
  error: (err: any) => console.log(`Error: ${err}`),
  complete: () => console.log('Stream completed')
};
```

![image](https://github.com/user-attachments/assets/33a0799e-958c-425d-8a14-9dd40c926c9c)

![image](https://github.com/user-attachments/assets/b0f02616-c444-40a0-a863-36145d1f34a9)

```typescript
import { BehaviorSubject } from 'rxjs';

// Create a BehaviorSubject with an initial value of 0
const behaviorSubject = new BehaviorSubject<number>(0);

// Subscriber 1
behaviorSubject.subscribe((value) => {
  console.log('Subscriber 1:', value);  // Will receive the most recent value (or initial value)
});

// Emit values
behaviorSubject.next(1);  // Subscriber 1 will receive 1
behaviorSubject.next(2);  // Subscriber 1 will receive 2

// Subscriber 2 (subscribes after some values were emitted)
behaviorSubject.subscribe((value) => {
  console.log('Subscriber 2:', value);  // Will receive the latest value (i.e., 2)
});

// Emit more values
behaviorSubject.next(3);  // Both Subscriber 1 and Subscriber 2 will receive 3
```

behavious subject tracks who the receivers are and who have received the data;


# change detection
<p>change detection refers to the mechanism used to track changes in the application's data model and reflect those changes in the user interface. In Angular 19 (or the latest versions of Angular), change detection continues to play a critical role in ensuring that the views are updated when the underlying model changes.</p>

![image](https://github.com/user-attachments/assets/e115db37-a3d0-42c4-bbbc-b6bee1cfea99)

```typescript
import { Component, ChangeDetectionStrategy } from '@angular/core';

@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  changeDetection: ChangeDetectionStrategy.OnPush
})
export class ExampleComponent {
  @Input() data: any;
}
```

![image](https://github.com/user-attachments/assets/00592695-950e-4df3-ba4f-62239f80a025)

```typescript
import { Component, ChangeDetectorRef } from '@angular/core';

@Component({
  selector: 'app-manual-detection',
  templateUrl: './manual-detection.component.html',
})
export class ManualDetectionComponent {
  constructor(private cdRef: ChangeDetectorRef) {}

  triggerChangeDetection() {
    this.cdRef.detectChanges();
  }

  markForCheck() {
    this.cdRef.markForCheck();
  }
}
```
<p>Angular uses Zone.js, a library that intercepts asynchronous operations (like setTimeout, Promises, etc.) and triggers change detection when such operations complete. However, in some cases, when interacting with external libraries or doing manual asynchronous operations, you may need to manually trigger change detection.</p>

![image](https://github.com/user-attachments/assets/f4c483a4-27ec-44bc-bca7-29afe415e66e)

![image](https://github.com/user-attachments/assets/d98b5111-4ea4-4075-93e9-88d62ed9dc38)

<p>both part of the change detection system, specifically used for comparing data structures that are iterable (like arrays) or objects. These differ types help Angular to efficiently detect changes in such data structures and update the DOM accordingly.</p>

# project architecture

![image](https://github.com/user-attachments/assets/625dacda-5306-4949-917c-70c7fd7af393)


to add environments ng g environments

![image](https://github.com/user-attachments/assets/083b9bf5-0567-4774-a788-1d8c2a5fca0d)
