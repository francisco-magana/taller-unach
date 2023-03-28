# Introducción

Angular es un framework de desarrollo web basado en TypeScript que permite el desarrollo veloz y escalable de interfaces de usuario mediante el uso de componentes. Este tutorial se centrará en enseñar los conceptos básicos de Angular, con especial atención en los temas de Vista, Clase y Estilos, Pipes y Servicios. Aprenderás cómo crear componentes, cómo interactúan las vistas con las clases y cómo utilizar estilos CSS para personalizar tus componentes. También explorarás el uso de Pipes para transformar datos en la vista y cómo los servicios permiten consumir API's. Este tutorial está pensado para ir de la mano de una expicación del instructor del taller para comentar a detalle cada uno de los pasos que se van siguiendo.


# ¿Porqué desarrollar una aplicación utilizando componentes?

- Modularidad: Los componentes son bloques de código independientes y reutilizables que encapsulan la lógica de negocio y la interfaz de usuario de una aplicación web. Esto permite que los desarrolladores puedan trabajar en diferentes componentes de forma separada y coordinada, lo que facilita el mantenimiento y la escalabilidad de la aplicación.

- Reutilización: Al utilizar componentes, los desarrolladores pueden crear bloques de código que se pueden reutilizar en diferentes partes de la aplicación. Esto reduce el tiempo y el esfuerzo necesario para desarrollar nuevas funcionalidades y mejora la consistencia y la coherencia de la aplicación.

- Separación de preocupaciones: Al separar la lógica de negocio y la interfaz de usuario en diferentes componentes, se reduce la complejidad del código y se mejora la legibilidad y la mantenibilidad de la aplicación. Además, esto permite que diferentes equipos de desarrollo puedan trabajar en diferentes partes de la aplicación sin interferir con el trabajo de otros equipos.

- Facilidad de prueba: Los componentes son bloques de código independientes que se pueden probar de forma aislada, lo que facilita la detección y corrección de errores y mejora la calidad y la fiabilidad de la aplicación.

- Escalabilidad: Al utilizar componentes, se puede agregar o quitar funcionalidades de la aplicación de forma más sencilla y rápida, lo que mejora la capacidad de la aplicación para crecer y adaptarse a nuevas necesidades y requerimientos.

# ¿Por qué Angular?

- Arquitectura robusta: Angular utiliza una arquitectura basada en componentes que separa claramente la lógica de negocio y la interfaz de usuario, lo que mejora la escalabilidad y mantenibilidad de la aplicación.

- TypeScript: Angular utiliza TypeScript, un lenguaje de programación que añade características adicionales a JavaScript, como la tipificación estática y otras características orientadas a objetos. Esto mejora la legibilidad y la seguridad del código y facilita el mantenimiento y la escalabilidad de la aplicación.

- Gran comunidad y documentación: Angular cuenta con una gran comunidad de desarrolladores y una amplia documentación, lo que facilita la resolución de problemas y la adopción de buenas prácticas.

- Herramientas integradas: Angular ofrece una gran cantidad de herramientas y características integradas, como la gestión de rutas, la inyección de dependencias, la validación de formularios, entre otras, que permiten a los desarrolladores crear aplicaciones web de forma más rápida y eficiente.

- Flexibilidad: Angular es un framework altamente flexible y adaptable a diferentes necesidades y requerimientos. Además, se puede integrar fácilmente con otras herramientas y tecnologías, lo que lo convierte en una herramienta muy útil para el desarrollo de aplicaciones web complejas.


# ¿Que necesitaremos para desarrollar este taller?

- NodeJS - Runtime de JavasCript para el servidor
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

Este tutorial esta pensado para ser muy sencillo, pero en caso de que te encuentres con una dificultad en tu camino, no dejes de persistir hasta resolver el problema o acercate a tu instructor para poder solucionarlo.

# Instalar angular CLI

## ¿Qué es Angular CLI?

Angular CLI es una herramienta de línea de comandos para desarrollar aplicaciones Angular. 

A continuación se presentan algunas de las principales funciones de Angular CLI:

1.  Creación de nuevos proyectos: Angular CLI proporciona un comando para crear un nuevo proyecto de Angular desde cero. Este comando configura automáticamente la estructura del proyecto y todas las dependencias necesarias para iniciar la construcción de una aplicación Angular.

2.  Generación de componentes: Angular CLI proporciona un comando para generar nuevos componentes de Angular en el proyecto. Este comando genera automáticamente los archivos de código fuente necesarios para crear un componente de Angular, como el archivo TypeScript, el archivo HTML y el archivo CSS.

3.  Generación de servicios: Angular CLI también proporciona un comando para generar servicios de Angular en el proyecto. Los servicios son una forma de proporcionar una funcionalidad reutilizable en una aplicación Angular, y el comando de generación de servicios de Angular CLI configura automáticamente los archivos de código fuente necesarios para crear un servicio de Angular.

4.  Compilación y ejecución: Angular CLI proporciona comandos para compilar y ejecutar una aplicación Angular. El comando de compilación de Angular CLI compila el código TypeScript en código JavaScript y genera una versión optimizada de la aplicación para producción. El comando de ejecución de Angular CLI inicia un servidor web local y muestra la aplicación en el navegador.

5.  Pruebas: Angular CLI proporciona comandos para ejecutar pruebas en una aplicación Angular. El comando de prueba de Angular CLI ejecuta todas las pruebas unitarias y de integración en la aplicación y proporciona informes detallados sobre

Instalamos mediante el gestor de paquetes `npm`:

```bash
npm install -g @angular/cli
```

Comprueba su instalación

```bash
ng version
```

Si haz obtenido respuesta de la interfaz de linea de comandos de angular...

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

Deberemos limpiar el contenido HTML del archivo 

```bash
app\app.component.html
```

Cuando tengamos una vista vacia, habrá que colocar un H1 con el texto que nosotros deseemos. Por ejemplo:

```html
<h1>¡Hola Angular!</h1>
```

¿Que vemos aquí? Discutamoslo mientras jugamos con poco con la compilación de Angular 👀

# Utilizando nuestro componente

En Angular, los componentes son la unidad básica de construcción de la interfaz de usuario. Los componentes son responsables de definir la estructura, el comportamiento y el estilo de una parte específica de la interfaz de usuario. Un componente típicamente se compone de los siguientes elementos:

1.  Clase de componente: es una clase de TypeScript que define la funcionalidad del componente, como sus propiedades, métodos y eventos. La clase de componente está decorada con un decorador `@Component` que le indica a Angular que esta clase es un componente.

2.  Plantilla: es un archivo HTML que define la estructura y el contenido del componente. La plantilla puede incluir datos dinámicos utilizando la sintaxis de interpolación `{{ }}` o directivas estructurales de Angular, como `*ngFor` o `*ngIf`.

3.  Estilos: son archivos CSS que definen el estilo del componente. Los estilos pueden ser globales o locales al componente.

## Modificando nuestra vista nuevamente

app.component.html
```html
<div class="text-centered">
  <h1 class="title">Hola mundo</h1>
</div>
```

Vemos los cambios

app.component.css
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

Volvemos a ver los cambios.

Hagamos unos cambios mas en la vista y en los estilos a nuestro gusto, la idea es que comprendamos como se relacionan estos elementos de la interfaz .

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

Una vez comprendido brevemente como es que la vista, los estilos y la clase TS estan relacionados entre si, continuemos.

# Actividad #1: Un contador

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

4.- Ajustamos nuestros estilos para dar un poco de vista a la aplicación.

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

5.- Agregamos una funcion al componente para aumentar el contador

```typescript
plus(): void {
    this.counter += 1;
}
```

6.- Modificamos el boton de sumar para poder utilizar esta función
```html
<button class="plus-button" (click)="plus()">+</button>
```

7.- Hacemos la función para decrementar el contador

```typescript
substract(): void {
    this.counter -= 1;
}
```

8.- Modificamos el boton de restar para poder utilizar esta función
```typescript
<button class="minus-button" (click)="substract()">-</button>
```

## Tenemos un contador funcional en pocos pasos

### ¿Puedes hacer un boton a cada lado que sume de 5 en 5 🤔?

¡INTENTALO!

![image](https://user-images.githubusercontent.com/64680073/228128950-3aa9f3a5-c6f0-47c7-bcc7-fe999ba697c1.png)

# Terminamos? Genial!

# Actividad #2: Guardar un historial

1.- Modificamos nuestro HTML para agregar un nuevo boton.

```html
<button class="plus-button">Save</button>
```

2.- Creamos una interfaz en Typescript para poder definir los datos del arreglo.

```typescript
interface historyRecord {
  count: number;
  date: Date
}
```

3.- Declaramos el arreglo

```typescript
history: historyRecord[] = [];
```

4.- Creamos una función sencilla para guardar en el historial mediante un push de un objeto.

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

## Listo, tenemos el historial en una variable que usaremos más adelante.

# Actividad #3: Creemos un nuevo componente para el historial

1.- Abrimos la terminal y detenemos el servidor de desarrollo con CTRL + C.

2.- Generamos un componente con ng generate component

```bash
ng g c components/list --skip-tests
```

¿Que vemos aquí?

-   "ng" se refiere al CLI de Angular.
-   "g" es la abreviatura de "generate", lo que significa que estamos generando un nuevo archivo o componente.
-   "c" es la abreviatura de "component", lo que significa que estamos generando un nuevo componente de Angular.
-   "components/list" es el nombre del nuevo componente que se está generando. En este caso, el nombre del componente es "list" y se colocará en la carpeta "components".
-   "--skip-tests" es una opción que se puede agregar al comando para indicar que no se deben generar archivos de prueba para el componente.

Por lo tanto, en resumen, el comando "ng g c components/list --skip-tests" genera un nuevo componente llamado "list" en la carpeta "components" de un proyecto Angular y omite la generación de archivos de prueba para el componente recién creado.

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

6.- Observamos nuevamente nuestra vista.

7.- Agregamos el app-list-item a app-list

```html
<p>list works!</p>
<app-list-item></app-list-item>
```

8.- Observamos nuestra vista nuevamente

9.- Ajustamos la vista del app-list-item

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

10.- Observamos nuestra vista

11.- Ajustamos el app-list

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

# Listo, continuemos

# Actividad #4: Recibamos el history en el list

1.- Agregamos la siguiente linea en el list.component.ts

```typescript
@Input() history: any[] = [];
```

2.- Modificamos el app-list de la vista de  app.component

```html
<app-list [history]="history"></app-list>
```

3.- Retiramos el console.log de la funcion de guardar el historial

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

# Puedes hacer que se reciban estos valores en el historial y se muestren bien? Intentalo












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


# Puedes agregar un boton adicional que limpie el historial? Intentalo


# TERMINAMOS CON NUESTRO TUTORIAL BASIQUISIMO DE ANGULAR 🥳🥳🥳

# PROYECTO 2: (Aún) Más funcionalidades de angular.
