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
