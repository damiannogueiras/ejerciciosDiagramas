### Examen de Programación (Funciones)
**Preguntas Teóricas:**

1.    **¿Cuál es el principal beneficio de usar la programación modular?**

    a)  Hace que el código sea más difícil de entender para los demás.    
    b)  Permite reutilizar código, facilita el mantenimiento y la depuración.    
    c)  Obliga a usar nombres de variables muy largos.  
    d)  Permite que el compilador se tome un descanso más largo.  


2.    **En C++, ¿cómo se implementan los subprogramas?**

    a)  Con instrucciones mágicas.  
    b)  Con funciones.  
    c)  Con hechizos y conjuros.  
    d)  Con poemas épicos.  

3.    **¿Qué es la "cabecera" de una función?**

    a)  La parte de arriba de un comentario.  
    b)  El tipo de valor devuelto, el nombre de la función y la lista de parámetros.  
    c)  Un sombrero que se pone el programador cuando crea la función.  
    d)  La directiva `#include`.  

4.    **¿Qué significa que una función sea de tipo `void`?**

    a)  Que no tiene alma.  
    b)  Que no devuelve ningún valor.  
    c)  Que solo puede ser llamada por fantasmas.  
    d)  Que está vacía y no hace nada.  

5.    **¿Cuál es la propiedad por la cual las funciones tienen la capacidad de llamarse a sí mismas?**

    a)  La arrogancia.  
    b)  La recursividad.  
    c)  La telepatía.  
    d)  El egocentrismo.  

6.    **¿Qué son los prototipos de función?**

    a) Una versión temprana e inacabada de la función
    b) La parte que describe la función pero no la implementa
    c) Funciones para imprimir código
    d) Versiones a escala para ver el diseño

7.    **En C++, ¿por qué es importante el orden en el que se declaran las funciones?**

    a) Para que el código se vea más bonito.  
    b) Porque el compilador necesita saber de la existencia de la función antes de usarla.  
    c) Porque si no el programa no se ejecutará durante la noche.  
    d) En realidad el orden no importa.  

8.    **¿Qué son los parámetros de una función?**

    a) Las variables que se utilizan solo para decorar la función.  
    b) Las variables locales a las que se les asigna un valor antes de ejecutar el cuerpo de la función.  
    c) Los nombres que usa la función para insultar a otras funciones.  
    d) Las condiciones climáticas necesarias para que la función se ejecute.  

9.    **¿Qué ocurre cuando se pasa un parámetro por valor a una función?**

    a) La función puede modificar la variable original.  
    b) Se realiza una copia del valor de la variable en el ámbito de la función.  
    c) La variable original se teletransporta al ámbito de la función.  
    d) El valor de la variable original se convierte en oro.  

10.   **¿Cuándo es útil el paso por referencia?**

    a) Cuando no te sabes el nombre de la variable que quieres modificar.  
    b) Cuando quieres modificar la variable original desde la función.  
    c) Cuando la variable original está muy lejos.  
    d) Cuando la variable original es demasiado grande para copiarla.  

**Preguntas con Código:**

11.   **¿Qué imprime este código?**

```c++
int suma(int a, int b) {
    return a + b;
}
int main() {
    int x = 5;
    suma(x, "hola");
    return 0;
}
```

    a) "8"  
    b) "Error de compilación: no se puede sumar un entero y una cadena.  "  
    c) "5hola"  
    d) "Depende de si la cadena es muy amigable"  

12.   **¿Qué imprime este código?**

```c++
void saludo() {
    cout << "Hola ";
}
int main() {
    int resultado = saludo();
    cout << resultado;
    return 0;
}
```

    a)  "Hola "
    b) "Hola 0"
    c)  "Error de compilación: no se puede asignar un `void` a un `int`.  "
    d) "Que tal?"

13.   **¿Qué imprime este código?**

```c++
int factorial(int n) {
    if (n == 0) return 1;
    else return n * factorial(n - 1);
}
int main() {
    cout << factorial(-1);
    return 0;
}
```

    a) Un numero grande, y seguramente se cuelgue
    b) Error
    c) Depende de si tienes mucho espacio en el stack
    d) 1
14.   **¿Qué imprime este código?**

```c++
void modificar(int x) {
    x = 100;
}
int main() {
    int y = 5;
    modificar(y);
    cout << y;
    return 0;
}
```

    a) "100"
    b) "5"
    c) Un error porque la función modifica sin devolver
    d) "Error! y no es un puntero"

15.   **¿Qué imprime este código?**

```c++
int valor_magico() {
    int valor = 42;
    return;
}
int main() {
    cout << valor_magico();
    return 0;
}
```

    a) 0
    b) Error porque la funcion no regresa nada
    c) Si la variable no es magica, no imprime nada
    d) Imprime el valor aleatorio que haya en memoria

16.   **¿Qué ocurre al ejecutar este código?**
```c++
void funcion_desconocida();
int main() {
    funcion_desconocida();
    return 0;
}
```

    a) Se imprime hola mundo
    b) Un error de compilacion
    c) El programa hace agua
    d) Se ejecuta pero realiza operaciones sin sentido

17.   **¿Qué imprime este código?**

```c++
#include <iostream>
using namespace std;
void imprimir(int arreglo[]) {
    cout << arreglo[0] << arreglo[1];
}
int main() {
    int numeros[] = {1, 2, 3};
    imprimir(numeros);
    return 0;
}
```

    a) "Error: el tamaño del arreglo no está especificado en la función".  
    b) "12"
    c) Depende del optimizador del compilador
    d) Nada.   La funcion se va de copas y se olvida de imprimir

18.   **¿Qué imprime este código?**

```c++
int calcular(int a, int b) {
  a = a * 2;
  return a + b;
}

int main() {
  int x = 5;
  int y = 10;
  int resultado = calcular(x, y);
  cout << x << " " << y << " " << resultado;
  return 0;
}
```

    a) 5 10 20
    b) 10 10 20
    c) Error de semántica
    d) Sale un unicornio en el cout

19.   **Este código, ¿qué imprime?**
```c++
void saludar(string saludo) {
    cout << saludo << " Mundo!";
}
int main() {
    saludar("¿Que tal?");
    return 0;
}
```

    a) ¿Que tal? Mundo
    b) error
    c) Dependede la configuracion regional
    d) Se inicia un holocausto

20.   **¿Qué imprime este código?**
```c++
int numeroMagico(int n) {
    if (n > 0) {
        return numeroMagico(n-1) + 1;
    } else {
        return 0;
    }
}
int main() {
    std::cout << numeroMagico(5) << std::endl;
    return 0;
}
```

    a) Error
    b) Depende del compilador
    c) 5
    d) Se invoca una entidad ancestral y se destruye el universo


