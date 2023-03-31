# Introducción

Angular es un framework de desarrollo web basado en TypeScript que permite el desarrollo veloz y escalable de interfaces de usuario mediante el uso de componentes. Este tutorial se centrará en enseñar los conceptos básicos de Angular, con especial atención en los temas de Vista, Clase y Estilos, Pipes y Servicios. Aprenderás cómo crear componentes, cómo interactúan las vistas con las clases y cómo utilizar estilos CSS para personalizar tus componentes. También explorarás el uso de Pipes para transformar datos en la vista y cómo los servicios permiten consumir API's. Este tutorial está pensado para ir de la mano de una explicación del instructor del taller para comentar a detalle cada uno de los pasos que se van siguiendo.

# ¿Por qué utilizar un framework para desarrollar una aplicación front end?

- **Productividad**: Los frameworks proporcionan herramientas y funcionalidades preconstruidas que permiten acelerar el proceso de desarrollo. Al utilizar estas herramientas, los desarrolladores pueden concentrarse en la lógica de negocio y las características únicas de la aplicación en lugar de tener que desarrollar todo desde cero.

- **Consistencia**: Los frameworks proporcionan un conjunto de reglas y convenciones que garantizan que el código sea coherente y fácil de mantener. Esto es especialmente importante cuando se trabaja en equipo, ya que garantiza que todos los desarrolladores estén siguiendo las mismas prácticas y estándares.

- **Mantenibilidad**: Los frameworks están diseñados para ser modulares y escalables, lo que facilita la adición de nuevas funcionalidades y la solución de problemas en el futuro. Esto permite a los desarrolladores realizar cambios de manera más rápida y eficiente en el futuro.

- **Comunidad de soporte**: Muchos frameworks tienen una gran comunidad de usuarios y desarrolladores que contribuyen al código y ofrecen soporte y recursos para el desarrollo. Esto significa que los desarrolladores pueden encontrar soluciones rápidas y efectivas para cualquier problema que puedan tener.

- **Actualizaciones regulares**: Los frameworks son actualizados regularmente para abordar problemas de seguridad, errores y agregar nuevas funcionalidades. Esto significa que los desarrolladores pueden mantenerse al día con las últimas tecnologías y mejores prácticas sin tener que investigar y actualizar el código manualmente.


# ¿Por qué desarrollar una aplicación utilizando componentes?

- **Modularidad**: Los componentes son bloques de código independientes y reutilizables que encapsulan la lógica de negocio y la interfaz de usuario de una aplicación web. Esto permite que los desarrolladores puedan trabajar en diferentes componentes de forma separada y coordinada, lo que facilita el mantenimiento y la escalabilidad de la aplicación.

- **Reutilización**: Al utilizar componentes, los desarrolladores pueden crear bloques de código que se pueden reutilizar en diferentes partes de la aplicación. Esto reduce el tiempo y el esfuerzo necesario para desarrollar nuevas funcionalidades y mejora la consistencia y la coherencia de la aplicación.

- **Separación de preocupaciones**: Al separar la lógica de negocio y la interfaz de usuario en diferentes componentes, se reduce la complejidad del código y se mejora la legibilidad y la mantenibilidad de la aplicación. Además, esto permite que diferentes equipos de desarrollo puedan trabajar en diferentes partes de la aplicación sin interferir con el trabajo de otros equipos.

- **Facilidad de prueba**: Los componentes son bloques de código independientes que se pueden probar de forma aislada, lo que facilita la detección y corrección de errores y mejora la calidad y la fiabilidad de la aplicación.

- **Escalabilidad**: Al utilizar componentes, se puede agregar o quitar funcionalidades de la aplicación de forma más sencilla y rápida, lo que mejora la capacidad de la aplicación para crecer y adaptarse a nuevas necesidades y requerimientos.

# ¿Por qué Angular?

- **Arquitectura robusta**: Angular utiliza una arquitectura basada en componentes que separa claramente la lógica de negocio y la interfaz de usuario, lo que mejora la escalabilidad y mantenibilidad de la aplicación.

- **TypeScript**: Angular utiliza TypeScript, un lenguaje de programación que añade características adicionales a JavaScript, como la tipificación estática y otras características orientadas a objetos. Esto mejora la legibilidad y la seguridad del código y facilita el mantenimiento y la escalabilidad de la aplicación.

- **Gran comunidad y documentación**: Angular cuenta con una gran comunidad de desarrolladores y una amplia documentación, lo que facilita la resolución de problemas y la adopción de buenas prácticas.

- **Herramientas integradas**: Angular ofrece una gran cantidad de herramientas y características integradas, como la gestión de rutas, la inyección de dependencias, la validación de formularios, entre otras, que permiten a los desarrolladores crear aplicaciones web de forma más rápida y eficiente.

- **Flexibilidad**: Angular es un framework altamente flexible y adaptable a diferentes necesidades y requerimientos. Además, se puede integrar fácilmente con otras herramientas y tecnologías, lo que lo convierte en una herramienta muy útil para el desarrollo de aplicaciones web complejas.


# ¿Qué necesitaremos para desarrollar este taller?

- NodeJS - Runtime de JavaScript para el servidor
- VScode o tu editor favorito 😉
- GIT - Control de versiones

Comprueba que cuentes con las herramientas mencionadas antes de comenzar, para ello, puedes ejecutar los siguientes comandos:

```bash
node --version
npm --version
git --version
```

# Antes de comenzar, ¿Qué pasa si algo no funciona como me dice el tutorial?

Es común que en el proceso de programación te encuentres con problemas o errores inesperados. En lugar de frustrarte, es importante que tengas la capacidad de buscar soluciones por tu cuenta. Esto no solo te hará un mejor programador, sino que te permitirá aprender nuevas habilidades y desarrollar tu capacidad de resolución de problemas. Recuerda que en el mundo de la programación siempre habrá desafíos, y enfrentarlos con una actitud amable y positiva te ayudará a superarlos de manera efectiva. Utiliza recursos como documentación, foros, tutoriales en línea y comunidades de programación para buscar soluciones y no dudes en pedir ayuda si es necesario. Con la práctica, pronto estarás resolviendo problemas con confianza y habilidad.

Este tutorial está pensado para ser muy sencillo, pero en caso de que te encuentres con una dificultad en tu camino, no dejes de persistir hasta resolver el problema o acércate a tu instructor para poder solucionarlo.

# Instalar angular CLI

## ¿Qué es Angular CLI?

Angular CLI es una herramienta de línea de comandos para desarrollar aplicaciones Angular. 

A continuación se presentan algunas de las principales funciones de Angular CLI:

1.  Creación de nuevos proyectos: Angular CLI proporciona un comando para crear un nuevo proyecto de Angular desde cero. Este comando configura automáticamente la estructura del proyecto y todas las dependencias necesarias para iniciar la construcción de una aplicación Angular.

2.  Generación de componentes: Angular CLI proporciona un comando para generar nuevos componentes de Angular en el proyecto. Este comando genera automáticamente los archivos de código fuente necesarios para crear un componente de Angular, como el archivo TypeScript, el archivo HTML y el archivo CSS.

3.  Generación de servicios: Angular CLI también proporciona un comando para generar servicios de Angular en el proyecto. Los servicios son una forma de proporcionar una funcionalidad reutilizable en una aplicación Angular, y el comando de generación de servicios de Angular CLI configura automáticamente los archivos de código fuente necesarios para crear un servicio de Angular.

4.  Compilación y ejecución: Angular CLI proporciona comandos para compilar y ejecutar una aplicación Angular. El comando de compilación de Angular CLI compila el código TypeScript en código JavaScript y genera una versión optimizada de la aplicación para producción. El comando de ejecución de Angular CLI inicia un servidor web local y muestra la aplicación en el navegador.

5.  Pruebas: Angular CLI proporciona comandos para ejecutar pruebas en una aplicación Angular. El comando de prueba de Angular CLI ejecuta todas las pruebas unitarias y de integración en la aplicación.

Instalamos mediante el gestor de paquetes `npm`:

```bash
npm install -g @angular/cli
```

Comprueba su instalación

```bash
ng version
```

Si has obtenido respuesta de la interfaz de línea de comandos de angular...

# ¡Estamos listos!

<hr>

## Iniciando un proyecto en su carpeta

```bash
ng new angular-unach
```

Al ejecutar el comando `ng new angular-unach`, Angular CLI realiza las siguientes acciones:

1.  Crea un nuevo directorio llamado `angular-unach`.
2.  Dentro de este directorio, crea una estructura de proyecto de Angular con los archivos y carpetas necesarios.
3.  Instala las dependencias necesarias de Angular, como el framework de Angular, RxJS, TypeScript y otras bibliotecas.
4.  Configura el proyecto con un archivo `tsconfig.json` para la compilación de TypeScript y un archivo `angular.json` para la configuración del proyecto de Angular.
5.  Crea un archivo `package.json` que incluye la información del proyecto y las dependencias instaladas.

Después de ejecutar este comando, se puede iniciar la construcción de una aplicación Angular dentro del directorio `angular-unach` utilizando otros comandos de Angular CLI, como `ng serve` para compilar y ejecutar la aplicación.

Ejecutamos:

```bash
ng serve
```

Al ejecutar el comando `ng serve`, Angular CLI realiza las siguientes acciones:

1.  Compila la aplicación Angular en código JavaScript, HTML y CSS.
2.  Inicia un servidor web local en el puerto 4200 por defecto, aunque este puede ser configurado con el parámetro opcional `--port`.
3.  Abre una ventana del navegador en la dirección `http://localhost:4200/`, que muestra la aplicación Angular en tiempo real.
4.  Observa los archivos del proyecto en busca de cambios, y cuando se detecta un cambio, Angular CLI recompila automáticamente la aplicación y la recarga en el navegador.

El comando `ng serve` es una herramienta muy útil para el proceso de desarrollo de aplicaciones Angular, ya que permite a los desarrolladores iterar rápidamente sobre la aplicación mientras se construye. También permite a los desarrolladores probar la aplicación en diferentes dispositivos y navegadores sin tener que desplegarla en un servidor remoto.

# Preparando nuestra vista

Deberemos limpiar el contenido HTML del archivo `app\app.component.html`

Cuando tengamos una vista vacía, habrá que colocar un H1 con el texto que nosotros deseemos. Por ejemplo:

```html
<h1>¡Hola Angular!</h1>
```

¿Qué vemos aquí? Discutamoslo juntos 👀

# Utilizando nuestro componente

En Angular, los componentes son la unidad básica de construcción de la interfaz de usuario. Los componentes son responsables de definir la estructura, el comportamiento y el estilo de una parte específica de la interfaz de usuario. Un componente típicamente se compone de los siguientes elementos:

1.  Clase de componente: es una clase de TypeScript que define la funcionalidad del componente, como sus propiedades, métodos y eventos. La clase de componente está decorada con un decorador `@Component` que le indica a Angular que esta clase es un componente.

2.  Plantilla: es un archivo HTML que define la estructura y el contenido del componente. La plantilla puede incluir datos dinámicos utilizando la sintaxis de interpolación `{{ }}` o directivas estructurales de Angular, como `*ngFor` o `*ngIf`.

3.  Estilos: son archivos CSS que definen el estilo del componente. Los estilos pueden ser globales o locales al componente.

## Modificando nuestra vista nuevamente

En nuestro app.component.html coloquemos el siguiente código:

```html
<div class="text-centered">
  <h1 class="title">Hola mundo</h1>
</div>
```

En los estilos, el archivo app.component.css agreguemos lo siguiente:
```css
.text-centered {
    display: flex;
    justify-content: center;
    align-items: center;
}

.title {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 48px;
    border-bottom: 8px solid black;
}
```

Hagamos unos cambios más en la vista y en los estilos a nuestro gusto, la idea es que comprendamos cómo se relacionan estos elementos de la interfaz.

## Usando la clase TS de nuestro componente

Creemos una variable en el archivo TS.

```typescript
readonly greeting: string = "Hola UNACH"
```

Usemos la variable en la vista

```html
<h1 class="title">{{ greeting }}</h1>
```

Hagamos este ejercicio con diferentes variables con distintos tipos de datos para observar sus resultados.

Una vez comprendido brevemente cómo es que la vista, los estilos y la clase TS están relacionados entre sí, comencemos con las actividades.

# Actividad #1: Un contador sencillo

1.- Deshagamos los cambios que hemos realizado anteriormente para poder comenzar la actividad.

2.- Declaramos una variable llamada counter en el component. 

```typescript
counter: number = 0;
```

3.- Ajustamos la vista para mostrar el contador y dos botones

```html
<div class="container">
  <button class="minus-button">-</button>
  <p class="counter">{{counter}}</p>
  <button class="plus-button">+</button>
</div>
```

4.- Agregamos nuestros estilos para dar un poco de vista a la aplicación.

```css
.container {
    height: 100vh;
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
}

.minus-button {
    background-color: tomato;
    padding: 32px;
    font-size: 48px;
    color: white;
    font-weight: bold;
    border: none;
    border-radius: 16px;
    transition: 0.3s;
    margin: 8px;
}

.minus-button:hover {
    background-color: red;
}

.plus-button {
    background-color: springgreen;
    padding: 32px;
    font-size: 48px;
    color: white;
    font-weight: bold;
    border: none;
    border-radius: 16px;
    transition: 0.3s;
    margin: 8px;
}

.plus-button:hover {
    background-color: green;
}

.counter {
    font-size: 48px;
    margin: 0px 32px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
```

5.- Agregamos una función al componente para aumentar el contador

```typescript
plus(): void {
    this.counter += 1;
}
```

6.- Modificamos el botón de sumar para poder utilizar esta función
```html
<button class="plus-button" (click)="plus()">+</button>
```

¿Que pasa si probamos la aplicación en este momento?

7.- Hacemos la función para decrementar el contador

```typescript
substract(): void {
    this.counter -= 1;
}
```

8.- Modificamos el botón de restar para poder utilizar esta función
```typescript
<button class="minus-button" (click)="substract()">-</button>
```

## Tenemos un contador funcional en pocos pasos 🎉🎉🎉

### ¿Puedes hacer un botón a cada lado que sume de 5 en 5 🤔?

¡INTENTALO!

![image](https://user-images.githubusercontent.com/64680073/228128950-3aa9f3a5-c6f0-47c7-bcc7-fe999ba697c1.png)

# ¿Terminamos? ¡Genial!

# Actividad #2: Guardar un historial

1.- Modificamos nuestro HTML para agregar un nuevo botón.

```html
<button class="plus-button">Save</button>
```

2.- Creamos una interfaz en Typescript para poder definir los datos del arreglo en el que guardaremos el historial.

```typescript
interface historyRecord {
  count: number;
  date: String
}
```

3.- Declaramos el arreglo como una variable utilizando la definción que realizamos anteriormente.

```typescript
history: historyRecord[] = [];
```

4.- Creamos una función sencilla para guardar en el historial mediante un push de un objeto al arreglo.

```typescript
  saveHistory(): void {
    this.history.push({
      count: this.counter,
      date: new Date().toLocaleString()
    });
    console.log(this.history)
  }
```

5.- La asignamos al botón

```html
<button class="plus-button" (click)="saveHistory()">Save</button>
```

## Listo, tenemos el historial en una variable que usaremos más adelante. Probemosla.

# Actividad #3: Creemos un nuevo componente para el historial

1.- Abrimos la terminal y detenemos el servidor de desarrollo con CTRL + C.

2.- Generamos un componente con ng generate component

```bash
ng g c components/list --skip-tests
```

¿Qué vemos aquí?

-   "ng" se refiere al CLI de Angular.
-   "g" es la abreviatura de "generate", lo que significa que estamos generando un nuevo archivo o componente.
-   "c" es la abreviatura de "component", lo que significa que estamos generando un nuevo componente de Angular.
-   "components/list" es el nombre del nuevo componente que se está generando. En este caso, el nombre del componente es "list" y se colocará en la carpeta "components".
-   "--skip-tests" es una opción que se puede agregar al comando para indicar que no se deben generar archivos de prueba para el componente.

El comando "ng g c components/list --skip-tests", entonces, genera un nuevo componente llamado "list" en la carpeta "components" y omite la generación de archivos de prueba para el mismo.

3.- Generamos un segundo componente

```bash
ng g c components/list-item --skip-tests
```

4.- Levantamos el servidor de desarrollo nuevamente

```bash
ng serve
```

5.- Insertamos el app-list en nuestro componente app.

```html
<div class="container">
  <button class="minus-button" (click)="substract5()">-5</button>
  <button class="minus-button" (click)="substract()">-</button>
  <p class="counter">{{counter}}</p>
  <button class="plus-button" (click)="plus()">+</button>
  <button class="plus-button" (click)="plus5()">+5</button>
  <br>
  <button class="plus-button" (click)="saveHistory()">Save</button>
</div>
<app-list></app-list>
```

6.- Observamos nuevamente nuestra vista. ¿Qué sucede?

7.- Agregamos el app-list-item a app-list

```html
<p>list works!</p>
<app-list-item></app-list-item>
```

8.- Observamos nuestra vista nuevamente. ¿Qué cambió?

9.- Realizamos los siguientes cambios a nuestro componente app-list-item

Vista
```html
<div class="item">
    <p>{{count}}</p>
    <p>{{date}}</p>
</div>
```

Clase
```typescript
export class ListItemComponent {
  count: number = 0;
  date: string = "12/12/2022, 12:12:12";
}
```

Estilos
```css
.item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    background-color: burlywood;
    margin: 25px 50px;
    padding: 8px;
    border-radius: 16px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: white;
}
```

10.- Observamos nuestra vista. ¿Qué observamos?

11.- Ahora modificaremos nuestro app-list

vista
```html
<h1 class="title">History</h1>
<div class="container">
    <app-list-item></app-list-item>
    <app-list-item></app-list-item>
    <app-list-item></app-list-item>
</div>
```

estilos
```css
.title {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    border-bottom: 6px solid black;
}

.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
```

### ¿Listo?, continuemos.

# Actividad #4: Recibamos el history en el list

1.- Agregamos la siguiente línea en el list.component.ts (presta atención a tu instructor para poder conocer como importar y donde colocar esta funcionalidad)

```typescript
@Input() history: any[] = [];
```

2.- Modificamos el app-list de la vista de app.component

```html
<app-list [history]="history"></app-list>
```

3.- Retiramos el console.log de la función de guardar el historial

```typescript
saveHistory(): void {
    this.history.push({
      count: this.counter,
      date: new Date().toLocaleString()
    });
  }
```

4.- Modificamos la vista de app-list de la siguiente manera

```html
<h1 class="title">History</h1>
<div class="container">
    {{history.toString()}}
</div>
```

5.- Observemos y entendamos el comportamiento

# Actividad #5: Mostrar el historial adecuadamente

1.- Modificamos la vista del app-list de la siguiente manera.

```html
<h1 class="title">History</h1>
<div class="container">
    <app-list-item *ngFor="let element of history"></app-list-item>
</div>
```

2.- Entendamos el comportamiento

# ¿Puedes hacer que se reciban estos valores en el historial y se muestren bien? Intentalo.

### ¿Listo? Continuemos.

1.- Agregamos estas dos variables al componente de app-list-item

```typescript
@Input() count: number = 0;
 @Input() date: string = "";
```

2.- Modificamos la vista de app-list

```html
<h1 class="title">History</h1>
<div class="container">
    <app-list-item *ngFor="let element of history" [count]="element.count" [date]="element.date"></app-list-item>
</div>
```

# ¿Puedes agregar un botón adicional que limpie el historial? Intentalo

# Los pipes

Continuemos con una práctica distinta a la anterior, sigamos los siguientes pasos:

1.- Iniciamos un nuevo proyecto de angular de la misma manera en que lo hicimos anteriormente.

```bash
ng new new-project

cd new-project

ng serve
```

2.- Limpiamos la vista de nuestro componente app

3.- Agregamos el siguiente código a la vista
```html
<div class="container">
  <div class="card">random text 1</div>
  <div class="card">random text 2</div>
  <div class="card">random text 3</div>
</div>
```

4.- Agregamos los siguientes estilos
```css
.container {
    display: flex;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    flex-wrap: wrap;
}

.card {
    border: 2px solid gray;
    border-radius: 8px;
    padding: 20px;
    font-size: 32px;
    width: 30%;
}
```

5.- Agregamos las siguientes variables a nuestro componente

```typescript
readonly name: string = "Soy francisco magana"
readonly age: number = 28;
readonly money: number = 12300.12;
```

6.- Las colocamos en los divs de la vista

```html
<div class="container">
  <div class="card">{{name}}</div>
  <div class="card">{{age}}</div>
  <div class="card">{{money}}</div>
</div>
```

7.- Agregamos nuestro primer pipe, como se muestra a continuación
```html
<div class="card">{{name | uppercase}}</div>
```
8.- ¿Qué está pasando?

En Angular, un "pipe" es una función que se utiliza para transformar los datos de un valor de entrada en otro valor de salida, de una forma determinada y predefinida.

Por ejemplo, puedes tener un valor numérico que quieres mostrar como una moneda, y para hacer esto puedes utilizar el pipe "currency". También puedes tener una fecha que quieres mostrar en un formato determinado, para lo que puedes utilizar el pipe "date".

Los pipes se utilizan en la plantilla HTML de Angular mediante el carácter "|" (pipe), seguido del nombre del pipe y, opcionalmente, de uno o varios argumentos entre paréntesis.

En resumen, un pipe en Angular te permite transformar datos de una forma fácil y eficiente para que se muestren de la forma que deseas en la interfaz de usuario.

9.- Agregamos los siguientes pipes para observar su comportamiento
```html
<div class="card">{{name | uppercase}}</div>
<div class="card">{{name | lowercase}}</div>
<div class="card">{{name | titlecase}}</div>
```

10.- Agregamos el siguiente pipe a los que ya tenemos
```html
<div class="card">{{age | percent}}</div>
```

11.- ¿Cómo hacemos que sea 20%? Intentalo

12.- Agregamos el siguiente pipe
```html
<div class="card">{{money | currency}}</div>
```

13.- Ahora agreguemos un cambio más y observemos que sucede ¿Son... parámetros?
```html
  <div class="card">{{money | currency:'USD'}}</div>
  <div class="card">{{money | currency:'EUR'}}</div>
  <div class="card">{{money | currency:'MXN'}}</div>
```

# Listo, fue muy sencillo ¿verdad?

Los pipes son herramientas muy útiles que nos ayudan a conseguir muchas cosas de manera sencilla y es un agregado de Angular que facilita el formateo de valores en la vista. Hay muchas cosas más que podemos hacer con los pipes, como el hecho de que podemos crear nuestros Pipes personalizados entre otras, sin embargo, no podemos abarcar todo en este taller, así que estás invitado a descubrir más acerca de los Pipes.

# Consumiendo una API con servicios

1.- Cerramos el servidor de angular con CTRL + C

2.- Ejecutamos el siguiente comando

```bash
ng g s services/using-api
```

3.- Arrancamos de nuevo el server

```bash
ng serve
```

4.- Importamos el HttpClientModule en el app.module
```typescript
import { HttpClientModule } from '@angular/common/http';
```

5.- Lo colocamos en los imports
```typescript
imports: [
    BrowserModule,
    HttpClientModule
  ],
```

¿Que acabamos de hacer? Escucha a tu instructor para una explicación detallada.

6.- Importamos el módulo `HttpClient` en el servicio que creamos

```typescript
import { HttpClient } from "@angular/common/http";
```

7.- Colocamos el módulo en el constructor
```typescript
constructor(public httpClient: HttpClient) { }
```

El parámetro "public httpClient" indica que se está inyectando el servicio HttpClient en la clase y se está declarando una variable llamada "httpClient" que puede ser utilizada en la misma.

HttpClient es un servicio proporcionado por Angular que permite realizar solicitudes HTTP, como GET, POST, PUT y DELETE, a un servidor remoto. Este servicio está diseñado para ser utilizado en aplicaciones web para recuperar datos de una API RESTful.

8.- Hacemos una función para hacer una request GET sencilla a una API pública de ejemplo
```typescript
makeRequest() {
    return this.httpClient.get('https://dummy.restapiexample.com/api/v1/employees');
  }
```

9.- Inyectamos el servicio en el app.component

```typescript
constructor(public api: UsingApiService) {}
```

10.- Ejecutamos la petición en el constructor de la siguiente manera
```typescript
constructor(public api: UsingApiService) {
    api.makeRequest().subscribe((res) => {
      console.log(res)
    })
  }
```
11.- ¿Qué está pasando?

Estamos realizando la llamada a la API mediante el servicio que hemos creado. Presta atención a tu instructor para poder comprender mejor cómo es que funcionan los observables en RXJS.

12.- Limpiemos la vista y agreguemos un botón para hacer la request

```html
<button (click)="request()">Make request</button>
```

13.- Actualicemos nuestro component

```typescript
  request() {
    this.api.makeRequest().subscribe((res) => {
      console.log(res)
    })
  }
  constructor(public api: UsingApiService) {}
```

14.- Detengamos el servidor con CTRL + C

15.- Creemos un nuevo componente para la tarjeta
```bash
ng g c components/card --skip-tests
```

16.- Arrancamos de nuevo el server
```bash
ng serve
```

17.- Modificamos la vista del componente que acabamos de crear
```html
<div class="card">
    <p>My name is {{name | titlecase}}</p>
    <p>My age is {{age}}</p>
    <p>My salary is {{salary | currency:'MXN'}}</p>
</div>
```

18.- Modificamos el componente
```typescript
@Input() name: string = "";
@Input() age: number = 0;
@Input() salary: number = 0;
```

19.- Modificamos los estilos
```css
.card {
    border: 2px solid black;
    border-radius: 8px;
    width: 30%;
}
```

20.- Modificamos el componente del app para obtener los resultados de la petición
```typescript
  results: any[] = [];

  request() {
    this.api.makeRequest().subscribe((res: any) => {
      this.results = res.data;
    })
  }
```

19.- La vista de app la dejaremos así
```html
<button (click)="request()">Make request</button>
<app-card *ngFor="let value of results" 
            [name]="value.employee_name" 
            [age]="value.employee_age"
        [salary]="value.employee_salary">
</app-card>
```

# Prestemos atención al instructor para terminar el taller y continuemos con ejemplos más sencillos con los conocimientos que hemos adquirido.
