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
