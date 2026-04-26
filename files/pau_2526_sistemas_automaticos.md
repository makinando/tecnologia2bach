# Problemas PAU - Curso 25/26

## Problemas de Sistemas Automáticos

Problemas tipo de la Ponencia de noviembre 2025, elaborados por la Comisión Estatal de Tecnología e Ingeniería II para la armonización nacional de la PAU curso 2025-26.

---

### Contenidos evaluables (Bloque F1)

1. Problemas sencillos de simplificación de sistemas mediante álgebra de bloques (conexiones en serie, paralelo, retroalimentación positiva y negativa, sin cambios de puntos de bifurcación).
2. Ventajas de los sistemas de control en lazo cerrado.
3. Papel que juega cada elemento en los sistemas de lazo cerrado (controlador, planta, sensor...).
4. Identificación de los elementos de un sistema de lazo cerrado en un sistema real.
5. Significado de la estabilidad o inestabilidad de un sistema de control.
6. Por qué un sistema estable en lazo abierto puede ser inestable en lazo cerrado.
7. Conocimiento general de los sensores, sin analizar su principio de funcionamiento.

> **Nota:** en cada problema se indica el contenido tratado con el número de epígrafe entre corchetes [X].

---

### Diagrama de bloques normalizado de referencia

El diagrama de bloques normalizado de un sistema de control en lazo cerrado es el siguiente:

![Diagrama de bloques normalizado](images/pau_2526_auto_diagrama.png)

Variables y bloques del diagrama:

- **c** — salida o variable controlada (temperatura, velocidad, presión...).
- **r** — señal de referencia o consigna (valor deseado de la salida).
- **e** — señal actuante o error: e = r – b.
- **b** — medida de la señal de salida.
- **m** — variable manipulada o de control.
- **p** — perturbación (señal externa de valor desconocido).
- **G₁** — controlador o regulador (la parte "inteligente" del sistema).
- **G₂** — planta o sistema controlado.
- **H** — elementos de medida de la salida (sensor de realimentación).

---

### Problema 1 [4]

Considerar la acción de control que lleva a cabo un conductor para mantener la velocidad de un vehículo a 80 km/h en una carretera con tramos llanos, subidas y bajadas. La velocidad es controlada mediante el pedal del acelerador y medida con un velocímetro digital. Se pide:

a) Identificar las señales y los bloques del diagrama de bloques normalizado con el sistema formado por el conductor, el vehículo y las características de la carretera.  
b) ¿Qué representaría la perturbación en el sistema propuesto?

---

### Problema 2 [4]

Con un grifo de cocina monomando se puede tener agua fría colocando la maneta en un extremo, muy caliente situándola en el otro extremo o una mezcla de ambas en el centro. El agua caliente procede de un termo eléctrico cuya temperatura a su salida no es constante. Considere la acción de control que lleva a cabo una persona para mantener manualmente la temperatura del agua en un valor constante como un sistema de control en lazo cerrado. Se pide:

a) Representar el sistema mediante un diagrama de bloques normalizado.  
b) Relacionar las variables y los bloques del diagrama con el sistema descrito.

---

### Problema 3 [4]

La figura muestra una cámara climática destinada a ensayos térmicos de componentes eléctricos. La temperatura de la cámara T es regulada en lazo cerrado mediante una resistencia calefactora cuya potencia P es suministrada por un circuito electrónico. Sabiendo que P = A·(T\* - T), donde T\* es la temperatura de referencia y A la ganancia del controlador, y que en régimen permanente T = T_amb + K·P, donde T_amb es la temperatura ambiente y K un parámetro constante de la cámara.

![Cámara climática y su diagrama de bloques](images/pau_2526_auto_prob3.png)

Se pide:

a) Completar el diagrama de bloques mostrado, indicando sobre él la variable manipulada, el controlador y la planta.  
b) Añadir un nuevo bloque al diagrama para representar las características del sensor de temperatura de la cámara.  
c) ¿Se podría considerar la T_amb como una perturbación? Justificar la respuesta.

---

### Problema 4 [1]

El diagrama de bloques mostrado corresponde al control de presión de un cilindro hidráulico. El transductor G₁ convierte la presión deseada p\* (introducida mediante un teclado) en la tensión v₁. En el punto de suma se resta a v₁ la tensión v₂ procedente de un sensor de presión colocado en el circuito hidráulico, y la diferencia v₃ se amplifica en G₂ y se aplica a la válvula G₃ que controla finalmente la presión del pistón.

![Diagrama de bloques control de presión cilindro hidráulico](images/pau_2526_auto_prob4.png)

Se pide:

a) Relación p/p\*.  
b) Si en régimen permanente G₂ = 10 V/V, G₃ = 25·10⁵ Pa/V y H = 0,1·10⁻⁵ V/Pa, obtener G₁ para que la presión del cilindro p sea igual a la de consigna p\*.

---

### Problema 5 [1]

El siguiente diagrama de bloques corresponde al control de velocidad de dos lazos de un motor eléctrico. x es la velocidad de referencia, y la velocidad real, e el error de velocidad, i la intensidad aplicada al motor, G₁ el controlador, G₂ el lazo de control de intensidad, G₃ el motor y H el medidor de velocidad (encoder). En régimen permanente: G₁ = 50 A/rpm, G₂ = 10, G₃ = 2 rpm/A y H = 1.

![Diagrama de bloques control de velocidad motor](images/pau_2526_auto_prob5.png)

Se pide:

a) Relación entre la velocidad real y la de consigna y/x.  
b) Error de velocidad (x - y) en rpm cuando x = 1.000 rpm.  
c) ¿Qué valor debe tomar H para que el error de velocidad sea cero?

---

### Problema 6 [1]

La figura muestra de forma simplificada un sistema para mantener constante la presión del agua en una vivienda. La presión deseada p\* (fijada mediante un potenciómetro y convertida a la tensión v₁) es comparada con la tensión v₂ procedente del sensor de presión colocado a la salida de la bomba. La diferencia de tensiones v₁ - v₂ es amplificada en G₂ y aplicada al motor de la bomba. G₃ representa la relación entre la presión de salida y la tensión v₄.

![Sistema control presión agua vivienda](images/pau_2526_auto_prob6.png)

Obtener la relación p/p\*.

---

### Problema 7 [1], [3]

La figura muestra en (a) el esquema de un termo eléctrico y en (b) su diagrama de bloques. El termo consta de un depósito de agua, una resistencia eléctrica calefactora, una sonda H que mide la temperatura del agua y la convierte a tensión con ganancia H = 0,1 V/ºC y un termostato. El termostato tiene un potenciómetro con mando giratorio para fijar la temperatura de consigna T\* en ºC y una salida de tensión m para la resistencia calefactora.

![Termo eléctrico y su diagrama de bloques](images/pau_2526_auto_prob7.png)

Se pide:

a) Obtener la relación T/T\* sin considerar la perturbación.  
b) Si en régimen permanente G₁ = 10 W/V, G₂ = 23 ºC/W y G₃ = H = 0,1 V/ºC, obtener el error de temperatura (T\* - T) cuando la temperatura de consigna es 60 ºC.  
c) ¿Qué función cumple el bloque G₃ en el diagrama?  
d) En el sistema térmico propuesto, ¿qué representaría la perturbación?

---

### Problema 8 [3]

Enumerar y comentar brevemente las principales características de los controladores proporcional, integral y derivativo.

---

### Problema 9 [3]

Una ducha convencional tiene un grifo monomando con el que se puede tener agua fría, caliente o una mezcla de ambas según la posición de la maneta. Considere la siguiente acción de control que lleva a cabo una persona para mantener manualmente la temperatura del agua en un valor constante: primero coloca el mando en una posición intermedia y comprueba que el agua sale fría. A continuación, mueve el mando para aumentar la temperatura y vuelve a comprobar que el agua sigue saliendo fría, repitiendo este proceso hasta alcanzar la temperatura ideal. Se pide:

a) Justificar qué tipo de control está realizando la persona: ¿P, PD o PI?  
b) Una vez conseguida la temperatura óptima, la persona nota que sin modificar el mando el agua se va enfriando. Entonces mueve la maneta rápidamente en previsión de una disminución más acentuada de la temperatura. ¿Qué acción de control está realizando la persona ahora? Justificar la respuesta.

---

### Problema 10 [3]

La figura muestra la entrada (error) y la salida (m) de dos tipos de controladores utilizados en sistemas de control de lazo cerrado. Indicar qué tipo de controlador es usado en cada uno de los casos.

![Gráficas de dos tipos de controladores](images/pau_2526_auto_prob10.png)

---

### Problema 11 [3]

La figura muestra un vehículo circulando con el control automático de la velocidad de crucero activado y fijado a 100 km/h. Las gráficas 1 y 2 muestran las velocidades, primero en llano y después en pendiente para dos controladores diferentes. En llano, la velocidad es prácticamente 100 km/h en ambos casos. Con el regulador 1 la velocidad decrece al tomar la pendiente y posteriormente retoma los 100 km/h; con el regulador 2 la velocidad se mantiene durante toda la pendiente en un valor inferior a 100 km/h.

![Gráficas control crucero reguladores 1 y 2](images/pau_2526_auto_prob11.png)

¿Qué tipo de regulador usa el control de crucero en el caso 1 y en el caso 2: P, PI o PD? Justificar la respuesta.

---

### Problema 12 [2], [3], [4], [7]

a) ¿En qué bloque o bloques del diagrama de bloques normalizado se incluirían los siguientes elementos?: motor eléctrico, cilindro neumático, controlador proporcional, fotocélula, potenciómetro, sonda PTC, tacómetro, regulador PID, termo eléctrico y teclado para introducir valores numéricos.  
b) Indicar dos ventajas y dos inconvenientes de los sistemas de control de lazo cerrado frente a los de lazo abierto.

---

### Problema 13 [5], [6]

¿Un sistema que es estable a lazo abierto puede ser inestable a lazo cerrado? Justificar la respuesta.

---

### Problema 14 [2], [7]

El alumbrado de un jardín se controla de forma automática mediante un sistema de lazo abierto compuesto por un interruptor de corte general, un programador horario para establecer las horas de encendido y apagado y un relé para el encendido de las lámparas controlado por el programador. Se pide:

a) Indicar qué elementos deben añadirse y cuáles deben eliminarse para convertirlo en un sistema de lazo cerrado.  
b) ¿Qué ventajas tiene el funcionamiento del alumbrado en lazo cerrado sobre el de lazo abierto?

---

### Problema 15 [5]

Durante el aprendizaje de montar en bicicleta se suele perder el equilibrio al mover el manillar en el sentido contrario al necesario para mantener la estabilidad. Se pide:

Explicar la relación que existe entre el manejo de la bicicleta durante el aprendizaje y la condición de estabilidad de un sistema en lazo cerrado.
