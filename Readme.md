### Test sobre Ficheros en C++

1 ****¿Cuál es la principal diferencia entre un fichero de texto y un fichero binario?****

    a) Los ficheros de texto solo almacenan letras.  
    b) Los ficheros binarios almacenan los datos en formato binario, los de texto en ASCII.  
    c) Los ficheros de texto son más eficientes.  
    d) No hay diferencia.  


2 **¿Qué librería de C++ es necesaria para trabajar con ficheros?**

    a) iostream
    b) stdio
    c) fstream
    d) fileio

3 **¿Qué clase se utiliza para escribir en un fichero?**

    a) ifstream
    b) ofstream
    c) fstream
    d) iofstream

4 **¿Qué clase se utiliza para leer de un fichero?**

    a) ifstream
    b) ofstream
    c) fstream
    d) ofile

5 **¿Qué método se utiliza para abrir un fichero?**

    a) open()
    b) create()
    c) file()
    d) fopen()

6 **¿Qué método se utiliza para cerrar un fichero?**

    a) close()
    b) end()
    c) finish()
    d) fclose()

7 **¿Qué significa la opción `ifstream::binary` al abrir un fichero?**

    a) Que el fichero es de texto.
    b) Que el fichero es binario.
    c) Que el fichero está encriptado.
    d) Que el fichero es de solo lectura.

8 **¿Qué operador se utiliza para escribir datos en un fichero de texto?**

    a) `<<`
    b) `>>`
    c) `=`
    d) `+`

9 **¿Qué operador se utiliza para leer datos de un fichero de texto?**

    a) `<<`
    b) `>>`
    c) `=`
    d) `-`

10 **¿Qué función se utiliza para leer una línea completa de un fichero de texto?**

    a) read()
    b) getline()
    c) get()
    d) scan()

11 **¿Qué método se utiliza para leer un solo byte de un fichero binario?**

    a) read()
    b) getline()
    c) get()
    d) scan()

12 **¿Qué método se utiliza para escribir un solo byte en un fichero binario?**

    a) write()
    b) put()
    c) print()
    d) insert()

13 **¿Qué método se utiliza para mover el puntero de lectura/escritura en un fichero?**

    a) move()
    b) seekg()
    c) shift()
    d) position()

14 **¿Qué indica el método `eof()`?**

    a) Si el fichero está abierto.
    b) Si se ha llegado al final del fichero.
    c) Si hay un error en el fichero.
    d) El tamaño del fichero.

15 **¿Qué significa "RAM"?**

    a) Random Access Memory
    b) Read Only Memory
    c) Real Access Memory
    d) Record Access Memory

16 **¿Qué es un "fichero" en el contexto de la programación?**

    a) Una carpeta en el disco duro.
    b) Un conjunto de datos almacenados en memoria secundaria.
    c) Una variable en el programa.
    d) Una función en el programa.

17 **¿Qué es más eficiente en términos de espacio, un fichero de texto o uno binario?**

    a) Un fichero de texto.
    b) Un fichero binario.
    c) Ambos son iguales.
    d) Depende del contenido.

18 **¿Qué paso es crucial al terminar de usar un fichero de escritura?**

    a) Abrirlo.
    b) Cerrarlo.
    c) Leerlo.
    d) Encriptarlo.

20 **¿Qué hace la función `fail()`?**

    a) Cierra el fichero.
    b) Comprueba si hay errores al abrir el fichero.
    c) Escribe en el fichero.
    d) Lee del fichero.

---

### Test Práctico con Estructuras de Control sobre Ficheros de Texto en C++

1.  **Apertura y Comprobación:** ¿Qué código verifica correctamente si un fichero "datos.txt" se ha abierto para lectura y muestra un mensaje de error si falla?
    *   a)
        ```cpp
        ifstream archivo("datos.txt");
        if (archivo) { /* continuar */ } else { cout << "Error"; }
        ```
    *   b)
        ```cpp
        ifstream archivo("datos.txt");
        if (archivo.fail()) { cout << "Error"; } else { /* continuar */ }
        ```
    *   c)
        ```cpp
        ifstream archivo("datos.txt");
        if (archivo.good()) { /* continuar */ } else { cout << "Error"; }
        ```
    *   d)
        ```cpp
        ifstream archivo("datos.txt");
        if (archivo.isOpen()) { /* continuar */ } else { cout << "Error"; }
        ```

2.  **Lectura Condicional:** ¿Qué código lee una línea del fichero "datos.txt" solo si el fichero está abierto correctamente?
    *   a)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        if (archivo.good()) { getline(archivo, linea); }
        ```
    *   b)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        if (archivo) { getline(archivo, linea); }
        ```
    *   c)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        getline(archivo, linea); // Siempre intenta leer
        ```
    *   d)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        while (archivo) { getline(archivo, linea); }
        ```

3.  **Escritura con `if`:** ¿Qué código escribe "Éxito" en "log.txt" solo si el fichero se abre correctamente?
    *   a)
        ```cpp
        ofstream log("log.txt");
        if (log.good()) { log << "Éxito"; }
        ```
    *   b)
        ```cpp
        ofstream log("log.txt");
        if (log) { log << "Éxito"; }
        ```
    *   c)
        ```cpp
        ofstream log("log.txt");
        log << "Éxito"; // Siempre escribe
        ```
    *   d)
        ```cpp
        ofstream log("log.txt");
        while (log) { log << "Éxito"; }
        ```

4.  **Bucle de Lectura:** ¿Qué bucle lee todas las líneas de un fichero llamado "datos.txt" e imprime cada línea en la consola?
    *   a)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        while (archivo.good()) { getline(archivo, linea); cout << linea << endl; }
        ```
    *   b)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        while (!archivo.eof()) { getline(archivo, linea); cout << linea << endl; }
        ```
    *   c)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        do { getline(archivo, linea); cout << linea << endl; } while (archivo);
        ```
    *   d)
        ```cpp
        ifstream archivo("datos.txt");
        string linea;
        for (int i = 0; i < 10; i++) { getline(archivo, linea); cout << linea << endl; }
        ```

5.  **Escritura Condicional con Bucle:** ¿Qué código escribe números del 1 al 5 en "numeros.txt", uno por línea, solo si el fichero se abre correctamente?
    *   a)
        ```cpp
        ofstream numeros("numeros.txt");
        if (numeros) { for (int i = 1; i <= 5; i++) { numeros << i << endl; } }
        ```
    *   b)
        ```cpp
        ofstream numeros("numeros.txt");
        for (int i = 1; i <= 5; i++) { numeros << i << endl; } // Siempre escribe
        ```
    *   c)
        ```cpp
        ofstream numeros("numeros.txt");
        while (numeros) { for (int i = 1; i <= 5; i++) { numeros << i << endl; } }
        ```
    *   d)
        ```cpp
        ofstream numeros("numeros.txt");
        if (numeros.isOpen()) { for (int i = 1; i <= 5; i++) { numeros << i << endl; } }
        ```

6.  **Lectura y Condición:** ¿Qué código lee un número del fichero "numero.txt" y muestra "Par" si es par, o "Impar" si es impar?
    *   a)
        ```cpp
        ifstream archivo("numero.txt");
        int num;
        archivo >> num;
        if (num % 2 == 0) { cout << "Par"; } else { cout << "Impar"; }
        ```
    *   b)
        ```cpp
        ifstream archivo("numero.txt");
        int num;
        if (archivo >> num) { if (num % 2 == 0) { cout << "Par"; } else { cout << "Impar"; } }
        ```
    *   c)
        ```cpp
        ifstream archivo("numero.txt");
        int num;
        if (archivo.is_open()) { archivo >> num; if (num % 2 == 0) { cout << "Par"; } else { cout << "Impar"; } }
        ```
    *   d)
        ```cpp
        ifstream archivo("numero.txt");
        int num;
        while (archivo >> num) { if (num % 2 == 0) { cout << "Par"; } else { cout << "Impar"; } }
        ```

7.  **Escritura con Bucle y Condición:** ¿Qué código escribe los números pares del 2 al 10 en "pares.txt"?
    *   a)
        ```cpp
        ofstream pares("pares.txt");
        for (int i = 2; i <= 10; i += 2) { pares << i << endl; }
        ```
    *   b)
        ```cpp
        ofstream pares("pares.txt");
        if (pares) { for (int i = 2; i <= 10; i++) { if (i % 2 == 0) { pares << i << endl; } } }
        ```
    *   c)
        ```cpp
        ofstream pares("pares.txt");
        int i = 2;
        while (i <= 10) { pares << i << endl; i += 2; }
        ```
    *   d)
        ```cpp
        ofstream pares("pares.txt");
        if (pares.good()) { for (int i = 2; i <= 10; i += 2) { pares << i << endl; } }
        ```

8.  **Lectura con `while` y `if`:** ¿Qué código lee números de "numeros.txt" y suma solo los números positivos?
    *   a)
        ```cpp
        ifstream archivo("numeros.txt");
        int num, suma = 0;
        while (archivo >> num) { if (num > 0) { suma += num; } }
        ```
    *   b)
        ```cpp
        ifstream archivo("numeros.txt");
        int num, suma = 0;
        while (!archivo.eof()) { archivo >> num; if (num > 0) { suma += num; } }
        ```
    *   c)
        ```cpp
        ifstream archivo("numeros.txt");
        int num, suma = 0;
        for (int i = 0; i < 10; i++) { archivo >> num; if (num > 0) { suma += num; } }
        ```
    *   d)
        ```cpp
        ifstream archivo("numeros.txt");
        int num, suma = 0;
        if (archivo) { while (archivo >> num) { if (num > 0) { suma += num; } } }
        ```

9.  **Escritura Condicional con Error:** ¿Qué código intenta abrir "datos.txt" para escritura y, si falla, escribe un mensaje de error en la consola?
    *   a)
        ```cpp
        ofstream archivo("datos.txt");
        if (!archivo.good()) { cout << "Error al abrir el fichero"; }
        ```
    *   b)
        ```cpp
        ofstream archivo("datos.txt");
        if (archivo.fail()) { cout << "Error al abrir el fichero"; }
        ```
    *   c)
        ```cpp
        ofstream archivo("datos.txt");
        if (!archivo.is_open()) { cout << "Error al abrir el fichero"; }
        ```
    *   d)
        ```cpp
        ofstream archivo("datos.txt");
        if (!archivo) { cout << "Error al abrir el fichero"; }
        ```

10. **Lectura y Escritura Condicional:** ¿Qué código lee líneas de "entrada.txt" y las escribe en "salida.txt" solo si ambas operaciones son exitosas?
    *   a)
        ```cpp
        ifstream entrada("entrada.txt");
        ofstream salida("salida.txt");
        string linea;
        if (entrada && salida) { while (getline(entrada, linea)) { salida << linea << endl; } }
        ```
    *   b)
        ```cpp
        ifstream entrada("entrada.txt");
        ofstream salida("salida.txt");
        string linea;
        while (getline(entrada, linea)) { salida << linea << endl; } // Siempre intenta
        ```
    *   c)
        ```cpp
        ifstream entrada("entrada.txt");
        ofstream salida("salida.txt");
        string linea;
        if (entrada.is_open() && salida.is_open()) { while (getline(entrada, linea)) { salida << linea << endl; } }
        ```
    *   d)
        ```cpp
        ifstream entrada("entrada.txt");
        ofstream salida("salida.txt");
        string linea;
        if (entrada.good() && salida.good()) { while (getline(entrada, linea)) { salida << linea << endl; } }
        ```




