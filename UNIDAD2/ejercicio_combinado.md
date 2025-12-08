<h1 align="center">🧮 Ejercicio Combinado — Unidad 2</h1>

---

<h2 align="center">📘 Explicación de los Lenguajes Utilizados</h2>

>En este ejercicio combinado se aplican los conocimientos de las estructuras algorítmicas utilizando de los dos lenguajes de programación: **Java** y **Python**. Pero el lenguaje elegido fue **Python**.

>A continuación, se presenta una explicación general de ambos lenguajes.

---

<h3 align="center">🐍 Python</h3>

>•	**Python:** Es un lenguaje de programación orientado a objetos de alto nivel, conocido por su sintaxis fácil de leer y de interpretar, lo que lo hace ideal para prototipado rápido y tareas [7]. Es ampliamente utilizado en computación científica, desarrollo web y automatización, siendo considerado un lenguaje amigable para principiantes pero potente para desarrolladores expertos a nivel global .*

>*Captura Nro.1: Sintaxis en Python (Hola, Mundo)***  
<p align="center">
  <em><img width="1487" height="326" alt="image" src="https://github.com/user-attachments/assets/34d99061-4f80-45d8-9b67-2d5d2b5ae966" /></em>
</p>

---

<h3 align="center">☕ Java</h3>

>•	Java: Es una plataforma informática y lenguaje de programación que reduce costos y tiempos de desarrollo, impulsando la innovación mediante servicios de aplicación robustos [8]. Se destaca por ser la plataforma de elección para empresas y desarrolladores debido a su fiabilidad y seguridad, permitiendo ejecutar aplicaciones tanto en entornos de escritorio como en grandes sistemas empresariales.

>*Captura Nro.2: Sintaxis en Java (Hola, Mundo)***  <p align="center">
  <em><img width="639" height="398" alt="image" src="https://github.com/user-attachments/assets/95d3e232-29b8-4728-862f-c7819fd2abb5" /></em>
</p>



---

<h2 align="center">🧩 Ejercicio Combinado "Python"</h2>

>**Nombre del Ejercicio:** Simulador de Entrenamiento - League of Legends

>Descripción del Problema: En el universo de Runaterra, se requiere desarrollar un sistema de entrenamiento para nuevos invocadores que permita simular y calcular el potencial de daño de sus campeones antes de entrar a la Grieta del Invocador.El sistema debe permitir al usuario seleccionar uno de los tres campeones disponibles (Aatrox, Sylas o Aphelios) para realizar una serie de pruebas de combate. Una vez seleccionado el personaje, el simulador debe ejecutar automáticamente 5 rondas de combate.En cada ronda, se debe calcular el daño final considerando las siguientes reglas de batalla:

>-Bonificación Ofensiva: El campeón activa su habilidad definitiva, la cual otorga inmediatamente un aumento del 55% sobre su poder base.

>-Defensa Enemiga: Existe la posibilidad de que el enemigo posea un "Amuleto Anulador". El sistema debe preguntar en cada ronda si el enemigo tiene este objeto.

>-Si el enemigo lo posee, el daño total del campeón se verá reducido en un 30%.

>-Si el enemigo no lo posee, el ataque impacta con toda su potencia.

>-**Integridad de la Simulación:** El sistema no debe permitir que se introduzcan datos erróneos (opciones de menú inexistentes o estados del amuleto inválidos), solicitando nuevamente la información hasta que sea correcta.

>-**Reporte de Impacto:** Al final de cada cálculo, el sistema debe clasificar el ataque en "Débil" (menor a 500), "Normal" (entre 500 y 1500) o "Crítico Legendario" (mayor a 1500).

---

<h3 align="center">📊 Diagrama de Flujo</h3>

<p align="center">
  <em><img width="674" height="995" alt="image" src="https://github.com/user-attachments/assets/9429998e-ed74-4ab1-ac95-9b44d6f0f50c" /></em>
</p>

---

<h3 align="center">💻 Código en Python</h3>

```python

print("--------------- Bienvenido a LOL RUNATERRA ----------------")
print("Para comenzar, tienes que elegir un personaje")
print("Presiona 'Enter', para empezar")
print("-----------------------------------------------------------")
input() # En Python input() pausa el programa hasta dar Enter (como getchar)

print("========== Lista de Personaje =============")
print("1. Aatrox (Luchador, cuerpo a cuerpo)")
print("2. Sylas (Magico, mago de control)")
print("3. Aphelios (ADC, pega a distancia)")
print("===========================================")

# En Python, el input siempre es texto, así que lo convertimos a entero (int)
opcion = int(input("Elige una opcion (1-3): "))

while opcion < 1 or opcion > 3:
    print("La lista de personaes es del 1-3, ingrese nuevamente: ")
    opcion = int(input())

# En Python no existe 'switch', 
# se usa if-elif-else para lograr lo mismo.
if opcion == 1:
    print("Has elegido a Aatrox. El Dios de los Darkins")
elif opcion == 2:
    print("Has elegido a Sylas. El Conquitador de Demacia")
elif opcion == 3:
    print("Has elegido a Aphelios. La luz de la Luna")
else:
    print("Error: Esa opcion no existe en la lista.")

# Estructura "For": range(1,6) significa del 1 hasta antes del 6 (es decir, 5 veces)
for i in range(1, 6):
    
    print(f"\n------------- RONDA DE BATALLA {i} --------------------")


    # Pedimos el dato por primera vez
    # Convertimos la entrada a decimal (float) para el poder
    poder_base = float(input("Ingrese el poder base del personaje: "))
    print("--------------------------------------------------------")
    
    # Aumento de poder (Habilidad Definitiva) (+55%)
    poder_aumentado = poder_base * 1.55
    print("Su personaje activo su habilidad definitva, su poder se aumenta en: ", poder_aumentado)
    print("----------------------------------------------------------")
    
    # Usamos int() porque esperamos un 1 o un 0
    tiene_amuleto = int(input("El enemigo tiene el 'Amuleto Anulador'? (1 = SI, 0 = NO): "))
    print("----------------------------------------------------------")
    
    # --- CONTROLAR LA ENTRADA CON WHILE ---
    # En Python '&&' se escribe como 'and'
    while tiene_amuleto != 0 and tiene_amuleto != 1:
        # Nota: En input() puedes poner el texto de la pregunta dentro
        tiene_amuleto = int(input(">> ERROR: Opcion invalida. Ingrese solo 1 (SI) o 0 (NO): "))
        print("--------------------------------------------------------")
        
    # --- ESTRUCTURA CONDICIONAL DOBLE (IF - ELSE) ---
    if tiene_amuleto == 1:
        # Reducción del 30%
        poder_final = poder_aumentado * 0.7
        print("-------------------------------------------------")
        print("[!] El enemigo activo su amuleto. Poder reducido.")
        print("-------------------------------------------------")
    else:
        # Poder intacto
        poder_final = poder_aumentado
        print("------------------------------")
        print("[+] El enemigo esta indefenso.")
        print("------------------------------")
        
    print("====================================")
    # Formato f-string: :.2f limita a 2 decimales (igual que %.2f en C)
    print(f">> Tu poder final de ataque es: {poder_final:.2f}")
    print("====================================")
    
    # Ponderacion del Daño
    # --- ESTRUCTURA MULTIPLE (IF - ELIF - ELSE) ---
    if poder_final < 500:
        print("-------------------------------------")
        print("RESULTADO: Ataque Debil.")
        print("-------------------------------------")
    elif poder_final >= 500 and poder_final < 1500:
        print("-------------------------------------")
        print("RESULTADO: Ataque Normal.")
        print("-------------------------------------")
    else:
        print("-------------------------------------")
        print("RESULTADO: !GOLPE CRITICO LEGENDARIO!")
        print("-------------------------------------")

```

<h3 align="center">✔️ Verificación </h3>

>*Captura Nro.3-4-5: Verificación de la Ejecución***

<p align="center">
  <em><img width="631" height="846" alt="image" src="https://github.com/user-attachments/assets/955eee93-65cc-408c-a39b-aac7e4b3dd8e" /></em>
</p>

<p align="center">
  <em>
<img width="631" height="846" alt="image" src="https://github.com/user-attachments/assets/4a586393-5ac5-4dac-a0b2-37c780de8fa3" /></em>
</p>

<p align="center">
  <em>
<img width="631" height="846" alt="image" src="https://github.com/user-attachments/assets/cc080cc4-dc6b-4ca7-adb8-cd1ebf75b328" /></em>
</p>

---
[⬅️ Volver al índice de la Unidad 2](../unidad2.md)




