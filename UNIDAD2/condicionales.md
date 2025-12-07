<h1 align="center">🔀 Estructuras Condicionales</h1>

> Las estructuras condicionales son esenciales porque permiten que un programa tome decisiones inteligentes, similares a las que tomamos en la vida diaria, evitando que la ejecución sea totalmente lineal [5]. Gracias a estas estructuras, el código puede adaptarse, reaccionar y elegir qué camino seguir según cada situación.

---

<h2 align="center">🟢 Estructura Simple (if)</h2>

### 📘 Definición de las estructuras simple

>•	**Estructura Simple (if):** Esta condición permite tomar una decisión simple: actúa solo si algo es verdadero. Si la condición no se cumple, el programa simplemente sigue adelante como si nada hubiera pasado.

---

### 📊 Ejercicio en Diagrama de Flujo 

<p align="center">
  <em><img width="400" height="600" alt="image" src="https://github.com/user-attachments/assets/d15d7503-699c-4853-8b50-2c084edc95b6" /></em>
</p>

### 💻 Ejercicio en C  

```python
#include <stdio.h>
int main(){

    float descuento, monto;

    printf("Porfavor, ingrese el monto de su compra: ");
    scanf("%f", &monto);

    if (monto < 500 ){
        printf("No se le realizo ningun descuento\n");
    } 
    
    if (monto >= 500 && monto <= 1000){
        descuento = monto * 0.95;
        printf("Se le realizo un descuento del 5%%, usted debe pagar: %.2f\n",descuento);
    }

    if ( monto > 1000){
        descuento = monto * 0.90;
        printf("Se le realizo un descuento del 10%%, usted debe pagar: %.2f\n",descuento);
    }
    
    return 0;
}

```
---

<h2 align="center">🟠 Estructura Doble (if – else)</h2>

### 📘 Definición de las estructuras dobles

<p align="center">
  <em><img width="500" height="600" alt="image" src="https://github.com/user-attachments/assets/d394d7c4-ae9a-4388-a97d-ac48705274e4" /></em>
</p>

>•	**Estructura Doble (if-else):** Ayuda a tomar decisiones de dos caminos: si la condición es verdadera, ejecuta una acción; si es falsa, ejecuta una alternativa. Es la forma natural de decir "si pasa esto, hago esto; si no, hago lo otro".

### 📊 Ejercicio en Diagrama de Flujo  


### 💻 Ejercicio en C

```python
#include <stdio.h>
int main(){

    float descuento, monto;

    printf("Porfavor, ingrese el monto de su compra: ");
    scanf("%f", &monto);

    if (monto < 500 ){
        printf("No se le realizo ningun descuento\n");
    } 
    
    if (monto >= 500 && monto <= 1000){ // Desde este punto, comienza la estructura doble
        descuento = monto * 0.95;
        printf("Se le realizo un descuento del 5%%, usted debe pagar: %.2f\n",descuento);
    }

    else { 
        descuento = monto * 0.90;
        printf("Se le realizo un descuento del 10%%, usted debe pagar: %.2f\n",descuento);
    } // Aqui termina la estructura doble
    
    return 0;
}
```

---

<h2 align="center">🔵 Estructura Múltiple (if – else if – else)</h2>

### 📘 Definición de las estructuras múltiples

>•	Estructura Múltiple (if-else if-else): Se utiliza cuando hay varias opciones posibles. El programa evalúa cada condición en orden hasta encontrar una verdadera, y si ninguna se cumple, ejecuta la acción final del else por defecto.

### 📊 Ejercicio en Diagrama de Flujo  

<p align="center">
  <em><img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/6abd559b-1eb0-41c1-ac12-570f41545b3d" /></em>
</p>

### 💻 Ejercicio en C  
```python
#include <stdio.h>
int main(){

    float descuento, monto;

    printf("Porfavor, ingrese el monto de su compra: ");
    scanf("%f", &monto);

    if (monto < 500 ){
        printf("No se le realizo ningun descuento\n");
    } 
    
    else if (monto >= 500 && monto <= 1000){ // Desde este punto, comienza la estructura doble
        descuento = monto * 0.95;
        printf("Se le realizo un descuento del 5%%, usted debe pagar: %.2f\n",descuento);
    }

    else { 
        descuento = monto * 0.90;
        printf("Se le realizo un descuento del 10%%, usted debe pagar: %.2f\n",descuento);
    } // Aqui termina la estructura doble
    
    return 0;
}

```
---

<h2 align="center">🔷 Switch Case en C</h2>

### 📘 Definición del Switch  
>El switch es una estructura de selección múltiple que evalúa una sola variable
y ejecuta un bloque según el valor que tenga.
Es más limpio y ordenado que usar muchos else if, pero solo funciona con:
✔ Enteros
✔ Caracteres
✔ Constantes predefinidas
. Es muy útil cuando hay muchas rutas claramente definidas.

### 📊 Ejercicio en Diagrama de Flujo (Switch) 

<p align="center">
  <em><img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/038e8f3f-114a-4b7e-a2ab-28e189176b4c" /></em>
</p>

### 💻 Ejercicio en C (Switch)  

```python
#include <stdio.h>

int main() {
    int opcion;

    // 1. Mostrar el menú
    printf("=== BIENVENIDO A MAC MCDONALD'S ===\n");
    printf("1. Cajita Feliz ($5.00)\n");
    printf("2. McCombo Grande ($8.00)\n");
    printf("3. McFlurry ($1.50)\n");
    printf("-----------------------------\n");
    printf("Elige una opcion (1-3): ");
    // 2. Leer la opción
    scanf("%i", &opcion);

    // 3. Estructura SWITCH
    switch (opcion) {
        case 1:
            printf("Has elegido la Cajita Feliz. Son $5.00\n");
            break; // El break evita que se ejecute el caso de abajo
       
        case 2:
            printf("McCombo Grande. Son $8.00\n");
            break;
            
        case 3:
            printf("Has elegido el McFlurry . Son $1.50\n");
            break;

        default: // Cierre de la Condicional SWITCH
            printf("Error: Esa opcion no existe en el menu.\n");
    }

    return 0;
}
```
---

[⬅️ Volver al índice de la Unidad 2](../unidad2.md)

