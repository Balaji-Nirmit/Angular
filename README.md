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
