<h1 align="center">🔁Estructuras Repetitivas</h1>

---

>Los bucles permiten repetir una tarea de forma automática sin hacerlo manualmente, haciendo el código más rápido, ordenado y eficiente [6]. Consisten en dar una instrucción que se repite mientras una condición siga siendo verdad .

---

<h2 align="center">🔢 Contadores y Acumuladores</h2>

>Los **contadores** y **acumuladores** son herramientas fundamentales dentro de los bucles.  
>✔ El **contador** sirve para llevar un registro de cuántas veces se repite un ciclo, normalmente aumentando en 1 cada vez.  
>✔ El **acumulador** permite ir sumando valores dentro del ciclo, como totalizar notas o acumular resultados.  
>Ambos permiten controlar el flujo del bucle y evitar errores como bucles infinitos o resultados incorrectos.

### 💻 Ejemplo en C
```c
#include <stdio.h>

int main(){

    int contador = 0;
    int acumulador = 0;

    while (contador < 5) { //Condicion
    acumulador += contador; //El acumulador, se va aumentado hasta igualar al contador
    contador++; //El contador, se va aumentado hasta cumplir la condicion
}
    return 0;
}

```

<h2 align="center">🟢 Bucle (While)</h2>

### 📘 Definición del bucle.

>“While”: Funciona repitiendo una acción siempre y cuando una condición se mantenga verdadera, similar a repetir algo mientras tenga sentido hacerlo.
---

### 📊 Ejercicio en Diagrama de Flujo 

<p align="center">
  <em><img width="400" height="600" alt="image" src="https://github.com/user-attachments/assets/57e29781-8093-412f-9882-e213899e472f" /></em>
</p>

### 💻 Ejercicio en C  

```C
#include <stdio.h>

int main() {
    
    int i = 1; 

    printf("--- Lista de Numeros ---\n");

    while (i <= 10) {
        printf("Numero: %i\n", i);
        i++; //Contador
    }

    printf("--- Fin de la lista ---");

    return 0;
}

```
---

<h2 align="center">🟢 Bucle (Do-While)</h2>


### 📘 Definición del bucle.

>“Do While”: A diferencia del anterior, aquí la acción se ejecuta al menos una vez antes de verificar la condición, asegurando que el usuario vea una primera ejecución antes de decidir si continuar.

### 📊 Ejercicio en Diagrama de Flujo  


<p align="center">
  <em><img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/a852b389-52d3-4ecb-a390-5647e76b6b70" /></em>
</p>


### 💻 Ejercicio en C

```C
#include <stdio.h>

int main() {
    
    int i = 1; 

    printf("--- Lista de Numeros ---\n");

    do{
        printf("Numero: %i\n", i);
        i++; //Contador
    } while (i <= 1);

    printf("--- Fin de la lista ---");

    return 0;
}

```

---

<h2 align="center">🔵 Bucle (For)</h2>

### 📘 Definición del bucle.

>"For:" Permite repetir una acción un número definido de veces siguiendo un orden específico, siendo ideal cuando necesitamos un proceso controlado y estructurado. Su funcionamiento se basa en tres partes fundamentales:

>Inicialización: Se establece el valor inicial del contador que marcará desde dónde empieza el ciclo.

>Condición: Se define la regla que determina cuántas veces se ejecutará el bucle, normalmente relacionada con el contador.

>Incremento o decremento: Se indica cómo cambiará el contador en cada repetición, conocido también como paso.

### 📊 Ejercicio en Diagrama de Flujo  

<p align="center">
  <em><img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/a7b7ae49-5126-4e30-a202-b4952fa162f6" /></em>
</p>

### 💻 Ejercicio en C  
```C
#include <stdio.h>

int main() {
    
    int i; 

    printf("--- Lista de Numeros ---\n");

    for (i = 1; i <= 10 ; i++){
        printf("Numero: %i\n", i );
    }
    
    printf("--- Fin de la lista ---");

    return 0;
}

```
---

[⬅️ Volver al índice de la Unidad 2](../unidad2.md)



