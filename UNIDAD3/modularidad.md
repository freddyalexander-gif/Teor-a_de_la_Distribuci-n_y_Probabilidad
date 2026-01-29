<h1 align="center">🧩 Programación Modular</h1>

---

<h2 align="center">📘 ¿Que es Programación Modular?</h2>

>La **programación modular** es una forma de organizar un programa dividiéndolo en partes más pequeñas llamadas **módulos, funciones o procedimientos**. Cada módulo cumple una tarea específica dentro del programa, lo que facilita la comprensión, el mantenimiento y la corrección de errores. Gracias a la modularidad, los programas se vuelven más ordenados y reutilizables, ya que un mismo módulo puede usarse varias veces sin necesidad de reescribir el código completo [9].

<h3 align="center">📌 Diagrama de su Estructura </h3>

>***Captura Nro.1: Se observa como un pograma principal Main (Nota Primer Ciclo), llama otras tareas mediante submódulos específicos.***
<p align="center">
  <img width="700" height="680" alt="image" src="https://github.com/user-attachments/assets/37187974-11a2-4407-9323-9c375621be50" />
</p>

<h3 align="center">📌 Funciones y Procedimiento </h3>

>>"Podemos aplicar la modularidad separando el código en dos tipos de bloques:

>-**Las Funciones:** Son como pequeñas máquinas que reciben información, hacen un cálculo y te devuelven una respuesta (útiles para operaciones matemáticas).

>***Captura Nro.2: Se puede oberservas una funcion del Main (Nota Primer Ciclo) en C, donde devuelve la nota del Promedio del ACD.***
<p align="center">
  <img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/f2d50fc6-5d25-4804-ac53-0e52155243de" />
</p>

>-**Los Procedimientos:** Son bloques que simplemente realizan una tarea (como borrar la pantalla) y terminan, sin necesidad de devolver un dato.

>***Captura Nro.3: Se puede oberservar una funcion void del Main (Zona Gamer) en C, donde presenta lo recaudado segun los clientes dados y al final presenta el reporte de ventas por la consola que han utilizado segun el numero de clientes.***
<p align="center">
  <img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/179b2ecf-b996-4974-abfb-22c98296412d" />
</p>

>-Para que el programa principal pueda enviar información a cualquiera de estos bloques, utilizamos los parámetros."


---

<h2 align="center">🔗 Parámetros por Valor y por Referencia</h2>

>En la programación modular, los **parámetros** permiten enviar información desde una parte del programa hacia un módulo, función o procedimiento. Dependiendo de cómo se envían estos datos, existen dos tipos principales de parámetros: **por valor** y **por referencia**.

<h3 align="center">🎞️ Animación del Proceso</h3>
<p align="center">
  <img src="https://i.sstatic.net/8XAQ1.gif" width="400" />
</p>

---

<h3 align="center">➡️ Parámetros por Valor</h3>

>El **parámetro por valor** consiste en enviar una copia del dato al módulo. Esto significa que el módulo trabaja con una versión temporal de la variable, por lo que cualquier cambio realizado dentro del módulo **no afecta al valor original**. Este tipo de parámetro es útil cuando se desea proteger los datos y evitar modificaciones no intencionales, manteniendo el control y la seguridad de la información.

>***Captura Nro.4: Se puede oberservar como las variables se envian mediante parametros de valor en C, donde en la segunda funcion lo unico que cambias es el orden de los numero sin cambiar al principal***
<p align="center">
  <img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/29c33d38-7465-4189-b473-2dbdf773237a"/>
</p>

>***Captura Nro.5: Ejecucion del Programa***
<p align="center">
  <img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/4cd129d9-ae9b-4268-aa4e-d676f95b6b4d" />
</p>

---

<h3 align="center">↔️ Parámetros por Referencia</h3>

>El **parámetro por referencia** permite que el módulo trabaje directamente con la variable original.En este caso, los cambios realizados dentro del módulo **sí afectan al valor original**, ya que no se envía una copia, sino una referencia a la ubicación del dato.Este tipo de parámetro es muy útil cuando se necesita modificar valores y devolver resultados sin usar variables adicionales [10].

>***Captura Nro.6: Se puede oberservar como las variables se envian mediante parametros de referencia en C, donde ambas funciones reciben los mismo parametros, tanto en el Main y el Void***

<p align="center">
 <img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/226531d7-653a-44f2-b8f7-6c66b849022a" /
</p>

>***Captura Nro.7: Ejecucion del Programa***
<p align="center">
<img width="300" height="500" alt="image" src="https://github.com/user-attachments/assets/6f763540-3e82-4698-bfe4-3034651d1662" />

</p>

---

[⬅️ Volver al índice de la Unidad 3](../unidad3.md)
