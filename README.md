# React Basic

Aprender conceptos basicos de React

## Docker (arranque recomendado)

Requisito: [Docker Desktop](https://www.docker.com/products/docker-desktop/).

```bash
# Desarrollo (hot-reload) → http://localhost:3000
docker compose --profile dev up --build

# Producción (nginx) → http://localhost:8080
docker compose --profile prod up --build
```

Para detener:

```bash
docker compose --profile dev down
# o
docker compose --profile prod down
```

## React

React puede ser muy útil para el desarrollo de aplicaciones web modernas e interactivas. React es una biblioteca de JavaScript de código abierto utilizada para construir interfaces de usuario (UI) interactivas y de una sola página. Fue creado por Facebook y lanzado en 2013. React se ha convertido en una de las herramientas más populares para la creación de aplicaciones web modernas y escalables, especialmente aquellas que manejan grandes cantidades de datos y requieren actualizaciones frecuentes. La principal ventaja de React es su capacidad para manejar y actualizar la interfaz de usuario en tiempo real sin tener que recargar la página completa. Utiliza un enfoque basado en componentes, lo que significa que las interfaces de usuario se descomponen en componentes pequeños y reutilizables, lo que facilita la creación y el mantenimiento de aplicaciones complejas. React también se integra fácilmente con otras bibliotecas y frameworks de JavaScript, como Redux y Angular. Esto permite a los desarrolladores construir aplicaciones personalizadas para satisfacer las necesidades específicas de su proyecto.

## Componentes de React

Los componentes son la piedra angular de React y son la forma principal en que se construyen las interfaces de usuario en React. Los componentes son como piezas de lego que se pueden ensamblar para crear una interfaz de usuario completa. En React, los componentes se pueden dividir en dos tipos: componentes funcionales y componentes de clase. Ambos tipos de componentes se crean con JavaScript y JSX (una extensión de sintaxis de JavaScript que permite escribir código HTML como código JavaScript). Los componentes funcionales son funciones que toman algunas propiedades (props) y devuelven elementos de React. Son más simples y fáciles de entender que los componentes de clase, pero no tienen estado propio (state) ni métodos de ciclo de vida. Los componentes de clase son clases de JavaScript que extienden la clase base React.Component. Estos componentes tienen estado propio y pueden tener métodos de ciclo de vida. Los componenetes basicamente son funciones que retornan una interfaz.

## Crear proeycto en React

1. Se requiere Node.js: React se ejecuta en Node.js, por lo que necesitas tener Node.js instalado en tu máquina. Puedes descargar la última versión de Node.js desde su sitio web oficial: https://nodejs.org. NPM (Node Package Manager): NPM es un gestor de paquetes de Node.js que se utiliza para instalar y administrar las dependencias de React. NPM se instala automáticamente cuando instalas Node.js.
2. Un editor de código: Necesitarás un editor de código para escribir y editar tu código de React. Hay muchos editores de código disponibles, como Visual Studio Code, Atom, Sublime Text, etc.
3. Instalar la herramienta: $ npm install -g create-react-app. Se puede verificar la version de la herramienta con: $ create-react-app --version
4. Crear el proeycto: $ create-react-app mi-aplicacion

## Comandos principales para crea un proyecto en React

- npm start: Este comando inicia el servidor de desarrollo y abre la aplicación en tu navegador predeterminado en http://localhost:3000. Cada vez que realices cambios en los archivos, la aplicación se recargará automáticamente.
- npm run build: Este comando crea una versión optimizada para producción de tu aplicación en la carpeta "build". Este proceso incluye la optimización del código, la creación de un archivo index.html y la copia de todos los archivos estáticos necesarios para la aplicación.
- npm test: Este comando ejecuta las pruebas de la aplicación utilizando el marco de prueba Jest.
- npm run eject: Este comando te permite expulsar tu aplicación de Create React App y proporciona acceso completo a la configuración y herramientas de construcción. Este comando es irreversible y no se recomienda a menos que sepas lo que estás haciendo.

## Estructura de un proyecto

- README.md: Archivo que describe la aplicación y su funcionamiento.
- node_modules/: Directorio que contiene todas las dependencias del proyecto, instaladas mediante npm.
- package.json: Archivo que contiene la información del proyecto, incluyendo las dependencias, los scripts, la versión, etc.
- public/: Directorio que contiene archivos públicos que no necesitan ser procesados por Webpack, como el archivo index.html.
- src/: Directorio que contiene el código fuente de la aplicación.
- App.css: Archivo que contiene estilos CSS específicos para el componente App.
- App.js: Archivo que contiene la lógica del componente App.
- App.test.js: Archivo que contiene pruebas para el componente App.
- index.css: Archivo que contiene estilos CSS para la página de inicio.
- index.js: Archivo principal que carga la aplicación y renderiza el componente App en el DOM.
- logo.svg: Archivo de imagen utilizado en el componente App.
- serviceWorker.js: Archivo que permite que la aplicación funcione sin conexión.
- setupTests.js: Archivo de configuración para Jest, utilizado para realizar pruebas.

## Webpack

Webpack es un paquete de módulos que se utiliza para construir aplicaciones web. Es una herramienta de construcción (build tool) que permite combinar múltiples archivos JavaScript y otros recursos (como CSS, imágenes y fuentes) en un único archivo que se puede enviar al navegador para su uso en una página web.

## JSX

JSX es una extensión de sintaxis para JavaScript que permite escribir código similar a HTML dentro de archivos de JavaScript. JSX es una parte integral de React y se utiliza para definir la estructura y el contenido de los componentes de React.

## Props

- Las props (abreviatura de "propiedades") son uno de los principales conceptos en React y se utilizan para pasar datos de un componente a otro. Las props son objetos que contienen datos y se pasan como argumentos a los componentes de React.
- defaultProps es una propiedad especial en React que se puede agregar a un componente de clase para establecer valores predeterminados para las props que el componente recibe. Si una prop no se proporciona al componente al ser utilizado, se usará el valor predeterminado especificado en defaultProps.
- PropTypes es una librería de validación de tipo para las props de los componentes en React. Permite al desarrollador especificar qué tipo de valor se espera que tenga cada prop, y proporciona una advertencia en tiempo de ejecución si se proporciona una prop con un tipo diferente al esperado.

## Hooks

React Hooks es una característica de React que permite a los desarrolladores usar el estado y otras características de React sin tener que escribir clases de componentes. Los hooks son funciones que permiten agregar estados y otras características de React a los componentes de función. Existen varios hooks integrados en React, algunos de los más comunes son:

- useState: permite agregar estado a un componente de función.
- useEffect: permite realizar tareas secundarias, como peticiones a API, después de que el componente se haya renderizado.
- useContext: permite acceder a un contexto global de la aplicación.
- useReducer: es similar a useState, pero para casos más complejos en los que el estado tiene una lógica más compleja.
- useCallback: permite optimizar el rendimiento de los componentes de función al memorizar las funciones que se pasan como propiedades.
- useMemo: permite optimizar el rendimiento de los componentes de función al memorizar valores computados.
- useRef: permite acceder al DOM o a cualquier valor mutable que se mantenga durante toda la vida del componente.

## Estructura de carpetas

- /src es la carpeta principal que contiene todos los archivos de código fuente de la aplicación y las demas carpetas son una subcarpeta de esta.
- La carpeta /components contiene todos los componentes reutilizables que se utilizan en diferentes páginas de la aplicación. Cada componente tiene su propia carpeta con un archivo index.js que exporta el componente, y los archivos ComponenteX.js y ComponenteX.css que contienen la lógica y la presentación del componente respectivamente.
- La carpeta /pages contiene todas las páginas de la aplicación. Al igual que en la carpeta /components, cada página tiene su propia carpeta con un archivo index.js que exporta la página, y los archivos PaginaX.js y PaginaX.css que contienen la lógica y la presentación de la página respectivamente.
- La carpeta /assets contiene todos los archivos de activos estáticos, como imágenes, fuentes, etc.
- Finalmente, App.js es el archivo principal que contiene la estructura general de la aplicación y la lógica común, index.js es el archivo de entrada de la aplicación, y index.css contiene las reglas de estilo globales de la aplicación.

## Tailwind css

Tailwind CSS es un framework de diseño de interfaz de usuario de código abierto que proporciona clases CSS predefinidas para ayudar en la creación de diseños personalizados rápidamente. En lugar de crear estilos personalizados desde cero, Tailwind CSS proporciona una serie de clases que pueden aplicarse a elementos HTML para modificar su estilo. Las clases en Tailwind están diseñadas para ser lo más comunes posible, lo que significa que no están vinculadas a un diseño o estilo específico. En su lugar, proporcionan una serie de utilidades para modificar y construir diseños complejos de manera más eficiente.
