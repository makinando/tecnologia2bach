# Problemas PAU - Curso 25/26

## Problemas Competenciales Contextualizados — Electrónica Digital

Problemas tipo de la Ponencia de noviembre 2025, elaborados por la Comisión Estatal de Tecnología e Ingeniería II para la armonización nacional de la PAU curso 2025-26.

---

### Contenidos evaluables (Bloque D2)

- Análisis y diseño de sistemas lógicos combinacionales: obtención de la tabla de verdad, determinación de la función lógica en forma de minterms y maxterms.
- Simplificación de la función lógica mediante el método de Karnaugh.
- Análisis, diseño e implementación de circuitos con puertas lógicas AND, OR, NOT, NAND y NOR.

---

### Problema 1 (versión 1)

Se dispone de un concentrador de agua de riego (F) al que llegan cuatro tuberías: tubería A (5 l/min), tubería B (10 l/min), tubería C (20 l/min) y tubería D (30 l/min). Cada tubería tiene un sensor que se activa cuando está pasando agua por ella. Se desea diseñar un circuito que detecte que al concentrador le llega un caudal superior o igual a 30 l/min. Se pide:

a) Obtener la tabla de verdad del circuito.  
b) Obtener la expresión simplificada del circuito.  
c) Dibujar el circuito lógico de la expresión simplificada.  
d) Razonar (basándose en la fórmula simplificada) si existe alguna entrada que no influya en el comportamiento del circuito.

---

### Problema 1 (versión 2)

Se dispone del mismo concentrador de agua de riego descrito en la versión 1. Se dispone de un circuito lógico con la siguiente tabla de verdad:

| A (5 l/min) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| B (10 l/min) | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 1 |
| C (20 l/min) | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 | 0 | 0 | 1 | 1 |
| D (30 l/min) | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 |
| F (≥ 30 l/min) | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 1 |

Se pide:

a) Obtener la fórmula simplificada del circuito.  
b) Dibujar el circuito lógico de la fórmula simplificada.  
c) Razonar (basándose en la fórmula simplificada) si existe alguna entrada que no influya en el comportamiento del circuito.  
d) ¿Cuál es el caudal mínimo que detecta el sistema? Justificar la respuesta.

---

### Problema 2

En una habitación se utiliza un sistema automatizado para controlar las luces (F) en función de tres entradas:

- Sensor de movimiento **M**: hay personas en la habitación = "1", no hay personas = "0".
- Sensor de luz ambiente **L**: luz insuficiente = "1", luz adecuada = "0".
- Interruptor manual **S**: encendido manual = "1", encendido automático = "0".

Las luces (F) se encenderán si: i) se detecta movimiento y la luz ambiente es insuficiente; ii) el interruptor manual está activado independientemente del resto de condiciones. Se pide:

a) Obtener la tabla de verdad y su función en forma canónica.  
b) Simplificar por el método de Karnaugh e implementar la función con puertas NAND.

---

### Problema 3

El sistema de seguridad de una guillotina para cortar papel tiene una salida (G) para el corte y una salida luminosa (A) de aviso. Consta, además, de dos pulsadores (I) y (D) y dos interruptores (M) y (E). Su funcionamiento es el siguiente:

- Si E está inactivo (E=0), la salida G no se activa en ningún caso (G=0).
- Si E=1 y M=1, la máquina funciona en modo seguro y es preciso que se pulsen simultáneamente ambos pulsadores (I=1; D=1) para que se active la salida (G=1) y se corte el papel.
- Si E=1 y M=0, la guillotina se activa pulsando cualquiera de los dos pulsadores (I o D) o ambos a la vez y, además, se activará la señal de aviso (A=1) para que el operario tenga cuidado durante esa operación.

![Sistema de control guillotina](images/pau_2526_dig_prob3.png)

Se pide:

a) Obtener la tabla de verdad y las funciones canónicas de G y A.  
b) Simplificar las funciones G y A por Karnaugh y obtener los correspondientes circuitos lógicos utilizando puertas NAND.

---

### Problema 4

En la figura, CD es un circuito digital que indica el nivel de agua de un depósito con tres leds. Si el líquido no llega a S1, no se enciende ningún led. Cuando el líquido llega a S1 (S1=1), solo se enciende L1 (L1=1); cuando el líquido llega a S2 (S2=1), solo se enciende L2 (L2=1; L1=0); cuando el líquido llega a S3 (S3=1), solo se enciende L3 (L3=1; L2=0; L1=0). Finalmente, si se da alguna combinación de la que se deduzca un fallo de detección de nivel, se encenderán los tres leds simultáneamente.

![Circuito detector de nivel con leds](images/pau_2526_dig_prob4.png)

Se pide:

a) Obtener la tabla de verdad y las funciones canónicas de los tres leds.  
b) Simplificar las funciones por Karnaugh y obtener los correspondientes circuitos lógicos por puertas básicas.
