---
title: 'Osciladores no sintonizados'
description: 'Vibrando entre dos mundos'
pubDate: 'Jun 23 2024'
heroImage: '/blog-placeholder-2.jpg'
---

El oscilador de puente de Wien es un oscilador RC no sintonizado de corrimiento de fase que utiliza retroalimentación tanto positiva como negativa. Es relativamente estable, de baja frecuencia y se sintoniza con facilidad. Se utiliza comúnmente en generadores de señal para producir frecuencias en el rango de 5 Hz a 1 MHz. Hewlett Packard utilizó este circuito en su diseño original de generador de señales.

![oscilador](/osciladores-2.png)

En la figura anterior, se muestra una red sencilla de adelanto-retraso. A la frecuencia de oscilación ( *f<sub>o</sub>* ), *R = X<sub>c</sub>* y la señal sufre un desplazamiento de fase de -45° a través de Z<sub>1</sub> y otro de +45° a través de Z<sub>2</sub> . En consecuencia, en *f<sub>o</sub>* , el desplazamiento total de fase a través de la red de adelanto-retraso es exactamente 0°. A frecuencias menores que la frecuencia de oscilación, el desplazamiento de fase a través de la red es de adelanto, y para frecuencias superiores, el desplazamiento se retrasa. A frecuencias extremadamente bajas C<sub>1</sub> funciona como circuito abierto, y no hay salida. A frecuencias extremadamente altas, C<sub>2</sub> funciona como un cortocircuito y no hay salida.

Una red de adelanto-retraso es un divisor reactivo de voltaje en el que el voltaje de entrada se divide entre Z<sub>1</sub> (la combinación de R<sub>1</sub> y C<sub>1</sub> en serie) y Z<sub>2</sub> (la combinación de R<sub>2</sub> y C<sub>2</sub> en paralelo). Por lo tanto, la red de adelanto-retraso es selectiva de frecuencia, y el voltaje de salida es máximo en *f<sub>o</sub>*. La función de transferencia (β) para la red de retroalimentación es igual a Z<sub>2</sub> / (Z<sub>1</sub> + Z<sub>2</sub>) y su máximo es igual a 1/3 en *f<sub>o</sub>*. 

![oscilador](/osciladores-3.png)

Esta figura muestra una gráfica de β en función de la frecuencia cuando *R<sub>1</sub> = R<sub>2</sub>* y *C<sub>1</sub> = C<sub>2</sub>*. Así, *f<sub>o</sub>* queda determinada por la siguiente ecuación:

- *f<sub>o</sub>* = 1 / 2π*RC*

en la que 
- R = R<sub>1</sub> = R<sub>2</sub>
- C = C<sub>1</sub> = C<sub>2</sub>

La figura a continuación:

![oscilador](/osciladores-4.png)

Es un oscilador con puente de Wien. La red de adelanto-atraso y el divisor resistivo de voltaje forman un puente de Wien (de donde procede el nombre de oscilador con puente de Wien). Cuando está balanceado el puente, la diferencia de voltaje es igual a cero. El divisor de voltaje proporciona una retroalimentación negativa o degenerativa, que compensa la retroalimentación positiva o regenerativa de la red de adelanto-atraso. La relación de los resistores en el divisor de voltaje es 2:1, y eso establece la ganancia de voltaje no inversor del amplificador *A<sub>1</sub>* , que es igual a *R<sub>f</sub>* / *R<sub>i</sub>* + 1 = 3. Así, en *f<sub>o</sub>* , la señal a la salida de +A<sub>1</sub>* se reduce en un factor de 3 al pasar por la red de adelanto-retraso (β = 1/3), y después se amplifica con factor de 3 en el amplificador *A<sub>1</sub>*. Por lo anterior, en *f<sub>o</sub>* , la ganancia de voltaje del lazo es igual a *A<sub>ol</sub>* β o sea 3 x 1/3 = 1.

El funcionamiento del circuito es el siguiente: en el encendido inicial aparece ruido (en todas las frecuencias) en *V<sub>sal</sub>* , que se retroalimenta por la red de adelanto-retraso. Sólo pasa ruido de *f<sub>o</sub>* por esa red con un desplazamiento de fase de 0°, y con relación de transferencia de 1/3 . En consecuencia, sólo se retroalimenta una sola frecuencia ( *f<sub>o</sub>* ) en fase, sufre una ganancia de voltaje de 1 en el lazo, y produce oscilaciones autosostenidas.
