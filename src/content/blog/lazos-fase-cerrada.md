---
title: 'Lazos de Fase Cerrada'
description: 'Comunicaciones electrónicas'
pubDate: 'Jun 29 2024'
heroImage: '/blog-placeholder-12.jpg'
---

<div style="text-align: justify;">
    <p>
        Los lazos de fase cerrada (PLL, por sus siglas en inglés) se utilizan ampliamente en las comunicaciones electrónicas para tareas como modulación, demodulación, generación de frecuencia y síntesis de señales. Estos sistemas se emplean tanto en transmisores como en receptores, ya sea para modulación analógica o digital, e incluso para la transmisión de pulsos digitales. Aunque los PLL se utilizaron por primera vez en 1932 para la detección síncrona de señales de radio, así como en circuitos de instrumentación y sistemas de telemetría espacial, inicialmente se evitó su uso debido a su tamaño, complejidad y costos. Sin embargo, con la llegada de la integración en gran escala, los PLL se han vuelto más compactos, fáciles de usar y confiables. En la actualidad, existen diversos productos con PLL integrados, diseñados para aplicaciones específicas como detección de tono, decodificación estereofónica y síntesis de frecuencias. En resumen, los PLL son una herramienta versátil y esencial en la electrónica moderna.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-5.png"/>
    </div>
    <p>
        En esencia, un PLL (lazo de fase cerrada) es un sistema de control retroalimentado en el que la frecuencia de la señal de voltaje retroalimentada es el parámetro clave, no solo el voltaje. Los PLL ofrecen sintonización selectiva y filtrado de frecuencia sin necesidad de bobinas o inductores. El circuito básico de un PLL consta de cuatro bloques principales:
    </p>
    <ul>
        <li><b>Comparador (Mezclador) de Fase:</b> Compara la fase y frecuencia de la señal de entrada con la frecuencia natural del VCO (oscilador controlado por voltaje).</li>
        <li><b>Filtro Pasabajas:</b> Filtra el voltaje de error generado por el comparador.</li>
        <li><b>Amplificador de Baja Ganancia:</b> Amplifica el voltaje filtrado.</li>
        <li><b>VCO:</b> Ajusta su frecuencia natural mediante un resistor y un capacitor externos. Cuando se aplica una señal de entrada al sistema, el PLL sincroniza el VCO con la señal de entrada. La frecuencia del VCO se iguala a la de la señal de entrada, con una diferencia finita de fase. Así, los PLL son como directores de orquesta electrónicos que mantienen la armonía entre las señales.</li>
    </ul>
    <p><b>El intervalo de enganche </b></p>
    <p>El intervalo de enganche se define como el margen de frecuencias cercanas a la frecuencia natural del VCO (oscilador controlado por voltaje) dentro del cual el PLL puede mantener la sincronización con una señal de entrada. En otras palabras, es el rango en el que el PLL sigue con precisión la frecuencia de entrada. Este intervalo también se conoce como intervalo de rastreo. La relación entre los intervalos de enganche y retención se ilustra en el diagrama de la figura 2-22. El límite inferior de enganche (fll) es la frecuencia mínima a la que el PLL puede rastrear, mientras que el límite superior de enganche (flu) es la frecuencia máxima de rastreo.</p>
    <p><b>El intervalo de captura</b></p>
    <p>El intervalo de captura se define como la banda de frecuencias cercanas a la frecuencia natural del VCO (oscilador controlado por voltaje) dentro de la cual el PLL puede establecer o adquirir sincronización con una señal de entrada. Por lo general, este intervalo está entre 1.1 y 1.7 veces la frecuencia natural del VCO. También se le llama intervalo de adquisición y está relacionado con el ancho de banda del filtro pasabajas. A medida que se reduce el ancho de banda del filtro, disminuye el intervalo de captura. El semiintervalo de captura es la mitad del intervalo máximo de captura (es decir, intervalo de captura menos semiintervalo de captura). En el diagrama de frecuencias de la figura 2-23 se ilustran estos intervalos y semiintervalos de captura. La frecuencia mínima a la que el PLL puede sincronizarse se denomina límite inferior de captura (fcl), mientras que la frecuencia máxima a la que puede engancharse se llama límite superior de captura (fcu). La relación entre los intervalos de captura, enganche, retención y semiintervalo de captura se muestra en el diagrama de frecuencias de la figura 2-24. Es importante destacar que el intervalo de captura nunca es mayor que el intervalo de enganche y que el intervalo de retención es igual al semiintervalo de captura.</p>
    <p><b>Oscilador controlado por voltaje</b></p>
    <p>
        Un oscilador controlado por voltaje (VCO, de voltage-controlled oscillator) es un oscilador (en forma más específica, un multivibrador de funcionamiento autónomo) con una frecuencia estable de oscilación, que depende de un voltaje de polarización externo. La salida de un VCO es una frecuencia, y su entrada es una señal de polarización o de control, que puede ser un voltaje de cd o de ca. Cuando se aplica un voltaje de cd o de ca de variación lenta en la entrada del VCO, la frecuencia de salida cambia, o se desvía, en forma proporcional. La fig. 2-25 muestra una curva de transferencia (frecuencia de salida en función de las características del voltaje de polarización en la entrada) de un VCO característico. La frecuencia de salida (fo) con voltaje de polarización de 0 V en la entrada es la frecuencia natural del VCO, fn, que está determinada por una red externa RC, y el cambio en la frecuencia de salida causado por un cambio de voltaje de entrada se llama desviación de frecuencia, f. En consecuencia, fo  fn  f, siendo fo  la frecuencia de salida del VCO. Para que haya una f simétrica, la frecuencia natural del VCO debe estar centrada en la parte lineal de la curva de entrada-salida.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-6.png"/>
    </div>
    <p>La función de transferencia de un VCO es:</p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-7.png"/>
    </div>
    <p>en la que</p>
    <ul>
        <li>K<sub>0</sub> = función de transferencia de entrada-salida (hertz por volt)</li>
        <li>ΔV = cambio de voltaje de control en la entrada (volts)</li>
        <li>Δf = cambio en la frecuencia de salida (hertz)</li>
    </ul>
</div>
