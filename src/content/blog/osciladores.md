---
title: 'Osciladores'
description: 'Vibrando entre dos mundos'
pubDate: 'Jun 15 2024'
heroImage: '/blog-placeholder-6.jpg'
---

<div style="text-align: justify;">
    <p>
        ¿Sabías que oscilar significa fluctuar entre dos estados? Un oscilador, entonces, es un dispositivo que produce estas oscilaciones, por consiguiente, oscilar es vibrar o cambiar, generando una forma de onda repetitiva. En el mundo de las comunicaciones electrónicas, los osciladores son esenciales, siendo utilizados en fuentes de portadora de alta frecuencia, fuentes piloto, relojes y circuitos de sincronización.
    </p>
    <p>
        Un oscilador en aplicaciones electrónicas produce oscilaciones eléctricas, cambios repetitivos de voltaje o corriente en una forma de onda. Si un oscilador es autosostenido, estos cambios son continuos y repetitivos. Los osciladores no autosostenidos, por otro lado, requieren una señal externa de entrada para producir un cambio en la forma de onda de salida.
    </p>
    <p>
        En esencia, un oscilador convierte un voltaje de entrada de corriente continua en un voltaje de salida de corriente alterna. La forma de la onda de salida puede variar, pero siempre se repite a intervalos periódicos. ¿Interesante, verdad?
    </p>
    <h5>Osciladores retroalimentados</h5>
    <p>Un oscilador retroalimentado es un amplificador con un lazo que permite que la energía fluya desde la salida y regrese a la entrada. Estos osciladores autosostenidos generan una señal de salida de corriente alterna, parte de la cual se regresa a la entrada para ser amplificada. Este proceso se repite, creando un ciclo regenerativo.</p>
    <p>Para que un circuito retroalimentado sostenga oscilaciones, debe cumplir con el criterio de Barkhausen: la ganancia neta de voltaje alrededor del lazo de retroalimentación debe ser igual o mayor que la unidad, y el desplazamiento neto de fase alrededor del lazo debe ser un múltiplo entero positivo de 360°.</p>
    <p>El oscilador retroalimentado requiere cuatro elementos: amplificación, retroalimentación positiva, componentes que determinan la frecuencia y una fuente de energía eléctrica.</p>
    <p>La amplificación se logra con al menos un dispositivo activo capaz de amplificar voltaje. La retroalimentación positiva asegura que la señal de salida regrese a la entrada con la fase y amplitud correctas para sostener las oscilaciones. Los componentes que determinan la frecuencia permiten ajustar o cambiar la frecuencia de operación. Finalmente, una fuente de energía eléctrica alimenta el oscilador.</p>
    <div style="display: flex; justify-content: center;">
        <img src="/2-3-b.png"/>
    </div>
</div>


- **Entrada (V<sub>1</sub>)**: esta es la señal que se introduce en el circuito.
- **Restador**: este componente toma la señal de entrada (V<sub>1</sub>) y la señal de retroalimentación (V<sub>4</sub>), y produce una nueva señal (V<sub>2</sub>) que se envía al amplificador.
- **Amplificador de voltaje (A<sub>ol</sub>)**: este componente amplifica la señal que recibe del restador.
- **Red de retroalimentación (β)**: esta parte del circuito toma una porción de la señal de salida (V<sub>sal</sub>) y la regresa al restador, creando un ciclo de retroalimentación.

Los osciladores retroalimentados tienen cuatro requisitos clave para funcionar:

- **Amplificación**: Necesitan al menos un dispositivo activo que pueda amplificar voltaje.
- **Retroalimentación positiva**: Deben tener una trayectoria completa para que la señal de salida regrese a la entrada. La señal de retroalimentación debe ser regenerativa, es decir, debe tener la fase correcta y la amplitud necesaria para sostener las oscilaciones.
- **Componentes que determinan la frecuencia**: Deben tener componentes que determinan la frecuencia, como resistores, capacitores, inductores o cristales.
- **Fuente de poder**: Necesitan una fuente de energía eléctrica, que puede ser una fuente de corriente continua (cd).

En estos sistemas, los voltajes de entrada y salida, junto con la ganancia de voltaje de lazo abierto (A<sub>ol</sub>), juegan un papel crucial. Las relaciones matemáticas que rigen estos sistemas son:

![oscilador](/ecuaciones-1.png)

Donde V<sub>1</sub> es el voltaje de entrada externa, V<sub>2</sub> es el voltaje de entrada al amplificador, V<sub>3</sub> es el voltaje de salida, V<sub>4</sub> es el voltaje de retroalimentación, A<sub>ol</sub> es la ganancia de voltaje de lazo abierto y β es la relación de retroalimentación del lazo de retroalimentación.

Estas ecuaciones nos llevan a una fórmula crucial para la ganancia de voltaje de lazo cerrado de un amplificador retroalimentado:
- A<sub>ol</sub> / (1 + βA<sub>ol</sub>)

Cuando βA<sub>ol</sub> baja a -1, el circuito oscilará y se podrá quitar la entrada externa. Para que se produzcan las oscilaciones autosostenidas, un circuito debe cumplir con los cuatro requisitos mencionados anteriomente, además de apegarse al modelo básico de circuito retroalimentado.

Aunque la acción de oscilador se puede lograr en muchas formas distintas, las configuraciones más comunes son las redes RC de desplazamiento de fase, los circuitos tanque LC (o circuitos LC resonantes), los cristales de cuarzo y los chips de circuito integrado. La clase de oscilación que se use en determinada aplicación depende de los siguientes criterios:

- Frecuencia necesaria de operación.
- Estabilidad requerida de frecuencia.
- Operación con frecuencia variable o fija.
- Requisitos o limitaciones de distorsión.
- Potencia necesaria en la salida.
- Tamaño físico.
- Aplicación (por ejemplo, digital o analógica).
- Costo.
- Fiabilidad y durabilidad.
- Exactitud necesaria.