---
title: 'Sintetizadores de Frecuencias'
description: 'Vibrando entre dos mundos'
pubDate: 'Jul 01 2024'
heroImage: '/blog-placeholder-13.jpg'
---

<div style="text-align: justify;">
    <p>
        Un sintetizador de frecuencias es un instrumento que, a partir de una frecuencia de referencia, permite obtener un conjunto discreto de frecuencias. Su objetivo es generar múltiples frecuencias de salida mediante operaciones como adición, sustracción, multiplicación y división de un conjunto limitado de frecuencias fijas. En términos sencillos, un sintetizador de frecuencias es un generador de frecuencia variable controlado por un cristal. El sintetizador ideal puede producir cientos o incluso miles de frecuencias distintas a partir de un solo oscilador de cristal, manteniendo la exactitud y estabilidad de cada frecuencia generada. Además, algunos sintetizadores pueden generar múltiples frecuencias de salida simultáneamente, todas sincronizadas con un único oscilador de referencia. Estos dispositivos se utilizan ampliamente en pruebas y mediciones (como generadores de señales de audio y RF), generadores de tonos (como los tonos DTMF), sistemas de control remoto, comunicaciones de varios canales y síntesis musical.
    </p>
    <h5>Sintetizadores directos de frecuencias</h5>
    <p>
        Sintetizador de frecuencias de cristal múltiple. La figura a continuación muestra un diagrama de bloques de un sintetizador de frecuencias de cristal múltiple que usa mezclado no lineal (heterodinaje) y filtrado, para producir 128 frecuencias distintas con 20 cristales y dos módulos de oscilador. Para los valores indicados de los cristales se sintetiza un intervalo de frecuencias de 510 kHz a 1790 kHz, en incrementos de 10 kHz. Un sintetizador como éste se puede usar para generar las frecuencias de portadora para las 106 estaciones de emisión de AM (de 540 kHz a 1600 kHz). Para las posiciones del conmutador que se indican, están seleccionados los osciladores de 160 kHz y 700 kHz, y las salidas del mezclador balanceado son sus frecuencias de suma y de diferencia (700 kHz  160 kHz  540 kHz y 860 kHz).
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-8.png"/>
    </div>
    <p>
        El filtro de salida se sintoniza a 540 kHz, que es la frecuencia de la portadora para el canal 1. Para generar la frecuencia de portadora para el canal 106 se selecciona el cristal de 100 kHz con el cristal de 1700 kHz (diferencia) o el de 1500 kHz (suma). La separación mínima entre frecuencias de salida en un sintetizador se llama resolución. La resolución del sintetizador de la figura es 10 kHz.
    </p>
    <h5>Sintetizadores indirectos de frecuencias</h5>
    <p>
        Sintetizadores de frecuencias con lazo de fase cerrada. En años recientes, los sintetizadores de frecuencias con PLL se han vuelto rápidamente el método más popularizado para síntesis de frecuencias. La figura a continuación muestra un diagrama de bloques para un sintetizador PLL de frecuencias de lazo sencillo. La referencia estable de frecuencia es un oscilador controlado por cristal. El intervalo de frecuencias generadas, y la resolución, dependen de la red divisora y de la ganancia de lazo abierto. El divisor de frecuencias es un circuito de dividir entre n, donde n es cualquier número entero. La forma más simple de circuito divisor es un contador digital de subida y bajada con frecuencia de salida fc  fo /n, donde fo es la frecuencia de salida del VCO.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/osciladores-7.png"/>
    </div>
    <p>
        Con este arreglo, una vez alcanzado el enganche, fc  fref, y la frecuencia de salida del VCO y el sintetizador es fo  nfref. Así, el sintetizador es esencialmente un multiplicador de frecuencia por n. El divisor de frecuencia reduce la ganancia de lazo abierto en un factor n. En consecuencia, los demás circuitos en torno al lazo deben tener ganancias relativamente altas. La ganancia de lazo abierto del sintonizador de frecuencias de la figura anterior es:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-7.png"/>
    </div>
    <p>
        Se puede ver en esta ecuación que cuando cambia n, la ganancia de lazo abierto cambia en proporción inversa. Una forma de remediar este problema es programar la ganancia del amplificador, así como la relación del divisor. Entonces, la ganancia de lazo abierto es:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-8.png"/>
    </div>
    <p>
        El intervalo de frecuencias con la frecuencia de referencia y el circuito divisor que se ven en la figura, es:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-9.png"/>
    </div>
    <p></p>
    <h5>Sintonizador de frecuencias preescalado</h5>
    <p>
        La figura a continuación muestra el diagrama de bloques de un sintetizador de frecuencias que usa un lazo de fase cerrada y un preescalador, para obtener división fraccionaria. También es necesario el preescalado para generar frecuencias mayores que 100 MHz, porque no se dispone de contadores programables que funcionen con eficiencia a esas altas frecuencias.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-9.png"/>
    </div>
    <p>
        El sintetizador de la figura usa un preescalador módulo dos. Tiene dos modos de operación. Un modo proporciona una frecuencia de salida por cada pulso P de entrada, y el otro modo proporciona una salida por cada pulso P + 1 de entrada. Cuando el registro m contiene un número distinto de cero, el preescalador cuenta en el modo P + 1. En consecuencia, una vez que los registros m y n se cargan inicialmente, el preescalador contará (P + 1)m veces hacia abajo, hasta que el contador m llegue a cero, el preescalador opera en el modo P y el contador n cuenta (n - m) veces hacia abajo. En este momento los contadores m y n se restablecen en sus valores originales, que se guardaron en los registros m y n, respectivamente, y se repite el proceso.  La ecuación de la frecuencia de salida del sintetizador, f<sub>o</sub> , es:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-10.png"/>
    </div>
</div>
