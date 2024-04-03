# Ejemplo de Uso de lambdas en C++

Introducción a las funciones lambda:

Las funciones lambda son una característica introducida en C++11 que permite definir funciones anónimas de manera concisa y flexible directamente en el lugar donde se necesitan.
Proporcionan una sintaxis más compacta que las funciones regulares, lo que hace que el código sea más legible y mantenible.
Sintaxis básica:

La sintaxis general de una función lambda es [capturas](parámetros) -> tipo_retorno { cuerpo }.

```cpp
      [capturas] (parámetros) -> tipo_retorno {
         // Cuerpo de la función lambda
      }

```cpp
   // Función lambda que suma dos números enteros
   auto suma = [](int a, int b) -> int {
      return a + b;
   };

### Corchetes [ ] (capturas):

   Los corchetes [ ] son utilizados para especificar las capturas, es decir, las variables externas que la función lambda puede utilizar. Hay tres tipos de capturas:
   [ ]: No captura ninguna variable externa.
   [nombre]: Captura la variable nombre por valor.
   [&nombre]: Captura la variable nombre por referencia.
   [=]: Captura todas las variables externas por valor.
   [&]: Captura todas las variables externas por referencia.
   Estas capturas permiten que la función lambda acceda a variables fuera de su ámbito local.

### Paréntesis () (parámetros):

   Los paréntesis () son utilizados para definir los parámetros de la función lambda, si es que los tiene. Funcionan de manera similar a los parámetros de una función regular.
   Flecha -> (tipo de retorno, opcional):

   La flecha -> es opcional y se utiliza para especificar el tipo de retorno de la función lambda. Si la función lambda tiene un cuerpo que incluye una declaración return, el tipo de retorno puede deducirse automáticamente y no es necesario especificarlo explícitamente.
   
### Cuerpo { } (implementación):

   El cuerpo { } de la función lambda contiene la implementación de la función. Es donde se especifica qué hace la función lambda cuando se ejecuta.
   Puede contener cualquier número de declaraciones y expresiones válidas en C++.
   La sintaxis y las reglas dentro del cuerpo son las mismas que las de una función regular.

Las funciones lambda son útiles en situaciones donde se necesitan funciones simples y anónimas, como en algoritmos de la STL (std::sort, std::transform, etc.) y algoritmos personalizados.
También son útiles en contextos donde se necesitan objetos funcionales, como en la programación funcional y el diseño de API modernas.
Flexibilidad y expresividad:

Las funciones lambda proporcionan flexibilidad y expresividad al permitir definir funciones de una manera más cercana al problema que se está resolviendo, evitando la necesidad de crear funciones globales o locales separadas.
Almacenamiento y paso de funciones lambda:

Las funciones lambda pueden ser almacenadas en variables y pasadas como argumentos a otras funciones, lo que las hace altamente versátiles y útiles en una variedad de contextos de programación.

## Cómo usar el Dockerfile

Para ejecutar el programa utilizando Docker, sigue estos pasos:

1. Asegúrate de tener Docker instalado en tu sistema.
2. Coloca el archivo `ListExample.cpp` y el Dockerfile en un mismo directorio.
3. Abre una terminal y navega hasta el directorio que contiene los archivos.
4. Construye la imagen del contenedor ejecutando el siguiente comando:

   ```
    docker build -t listexample .
   ```

5. Una vez que se complete la construcción de la imagen, puedes ejecutar el programa en un contenedor Docker utilizando el siguiente comando:

   ```
    docker run -it --rm listexample
   ```