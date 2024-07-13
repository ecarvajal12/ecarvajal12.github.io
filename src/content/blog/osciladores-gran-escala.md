---
title: 'Osciladores en Gran Escala de Integración'
description: 'Vibrando entre dos mundos'
pubDate: 'Jun 27 2024'
heroImage: '/blog-placeholder-11.jpg'
---

<div style="text-align: justify;">
    <p>
        En los últimos años ha aumentado con una rapidez asombrosa el uso de los circuitos con integración a gran escala (LSI, de large scale integration) para generar frecuencias y formas de onda, porque los osciladores de circuito integrado tienen una excelente estabilidad de frecuencia y un amplio margen de sintonía, y por ser fáciles de usar. Los generadores de forma de onda y los generadores de funciones se usan en forma extensa en equipos de comunicaciones y de telemetría.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-1.png"/>
    </div>
    <p>
        En laboratorios y equipos de prueba, los osciladores y generadores de funciones comerciales se encuentran en forma de circuitos integrados monolíticos (LIC). Estos LIC ofrecen una alternativa de bajo costo a sus contrapartes no integradas. Imagina a estos pequeños chips como orquestas compactas: reúnen una gran cantidad de dispositivos activos en un solo CI. Además, su compensación térmica y seguimiento preciso de los valores de los componentes los hacen aún más atractivos. Hoy en día, los generadores de forma de onda LSI (con integración en gran escala) rivalizan con los generadores discretos complejos, pero a una fracción del costo. Así que, cuando veas un oscilador en acción, piensa en esta sinfonía electrónica que se despliega en un espacio diminuto.
    </p>
    <h5>Generación de forma de onda con circuito integrado</h5>
    <p>
        En su forma más sencilla, un generador de forma de onda es un circuito oscilador que produce formas de onda precisas y estables. Estas formas de onda pueden ser moduladas o barridas externamente dentro de un rango específico de frecuencia. Un generador típico consta de cuatro secciones básicas:
    </p>
    <ul>
        <li><b>Oscilador:</b> Genera la forma de onda periódica fundamental.</li>
        <li><b>Conformador de Onda:</b> Transforma la señal cruda del oscilador en una forma específica (senoidal, cuadrada, triangular o en rampa).</li>
        <li><b>Modulador (opcional):</b> Permite la modulación de amplitud (AM) al superponer una señal de baja frecuencia.</li>
        <li><b>Amplificador Separador:</b> Aísla al oscilador de la carga externa y proporciona la corriente necesaria.</li>
    </ul>
    <p>
        La siguiente figura muestra un diagrama simplificado de bloques de un circuito generador de forma de onda con circuito integrado. Cada sección se ha fabricado por separado en forma monolítica durante varios años, y la integración de estas secciones en un solo circuito monolítico fue una evolución natural de la tecnología existente. En resumen, este proceso crea melodías electrónicas dentro de un pequeño chip.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-2.png"/>
    </div>
    <p>
        Un circuito integrado oscilador usa la carga y descarga de corriente constante de capacitores externos de temporización. La figura a continuación muestra el esquema simplificado de uno de estos generadores de onda, que usa un multivibrador acoplado por el emisor, que es capaz de generar ondas cuadradas, así como las formas triangular y de rampa lineal.
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/circuito-3.png"/>
    </div>
    <p> 
        El circuito funciona como sigue. Cuando el transistor Q1 y el diodo D1 conducen, el transistor Q2 y el diodo D2 están apagados y viceversa. Esta acción carga y descarga alternativamente al capacitor Co con la fuente de corriente constante I1. El voltaje a través de D1 y D2 es una onda cuadrada simétrica con amplitud de pico a pico igual a 2VBE. VA es constante cuando Q1 está activo, pero se transforma en una rampa lineal con pendiente igual a I1/Co cuando Q1 se apaga. La salida VB(t) es idéntica a VA(t), excepto que está demorada medio ciclo. La salida diferencial, VA(t) VB(t) es una onda triangular. La figura anterior muestra las formas de onda de voltaje de salidad que se producen en forma normal.
    </p>
    <p>
        El XR-2206 es un generador de funciones en circuito integrado monolítico fabricado por EXAR Corporation. Este versátil dispositivo es capaz de producir formas de onda de alta calidad, incluyendo senoidales, cuadradas, triangulares, de rampa y de pulso. Además, ofrece un alto grado de estabilidad y precisión.
    </p>
    <p>
        Las formas de onda de salida del XR-2206 pueden ser moduladas tanto en amplitud como en frecuencia mediante una señal moduladora externa. La frecuencia de operación se puede seleccionar externamente dentro de un rango que abarca desde 0.01 Hz hasta más de 1 MHz.
    </p>
    <p>
        Este circuito integrado es especialmente adecuado para aplicaciones en comunicaciones e instrumentación. Así que, la próxima vez que necesites generar formas de onda precisas, piensa en el XR-2206 como un director de orquesta electrónico dentro de un pequeño chip.
    </p>
     <div style="display: flex; justify-content: center;">
        <img src="/circuito-4.png"/>
    </div>
    <p>
        El <b>XR-2206</b> es un generador de funciones que produce ondas senoidales, cuadradas y triangulares. Su estabilidad normal de frecuencia es de 20 ppm/°C, y se puede barrer linealmente con un voltaje externo de control en un amplio intervalo de frecuencias (hasta 2000:1). Este circuito integrado es ideal para aplicaciones en comunicaciones e instrumentación. Las fórmulas para determinar las dos frecuencias de operación son:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-4.png"/>
    </div>
    <ul>
        <li>R1 resistor conectado con la terminal 7</li>
        <li>R2 resistor conectado con la terminal 8</li>
    </ul>
    <p>
        La frecuencia de oscilación es proporcional a la corriente total de sincronización en la terminal 7 o en la 8. La frecuencia varía en forma lineal con la corriente, dentro de un intervalo de valores de corriente de 1 a 3 µA. Esta frecuencia se puede controlar aplicando un voltaje de control VC a la terminal seleccionada de sincronización. La frecuencia de oscilación se relaciona con VC mediante la ecuación:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-5.png"/>
    </div>
    <p>
        La ganancia K, de conversión de voltaje a frecuencia, se determina con:
    </p>
    <div style="display: flex; justify-content: center;">
        <img src="/ecuaciones-6.png"/>
    </div>
</div>

