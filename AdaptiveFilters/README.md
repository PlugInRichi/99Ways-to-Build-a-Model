# Filtros Adaptativos
Imginemos el siguiente problema:
Deseamos estimar una señal a partir de otra pero solo tenemos acceso a la segunda, muy probablemente la señal que deseamos estimar se encuentra mezclada con otras señales, ruido ambiental o es modificada por el canal de transmisión. ¿Cómo podemos separar la señal de interés del resto de señales?

### Modelos de predicción lineal 
Supongamos una señal descrita de forma recursiva por sus valores anteriores 
$$ d(n) = a_1 d(n-1) + a_2 d(n-2)  + ... +a_k d(n-k) $$

Si deseamos transmitir esta señal de forma discreta es posible añadir ruido a la señal de tal manera que a simple vista no sea perceptible la existencia del modelo de la señal original $d(n)$

$$ x(n) = d(n) + v(n) $$

Un receptor es capaz de captar la señal $x(n)$ sin embargo desconoce el modelo de la señal original que fue enviada. Para recuperar los coeficientes que describen al la señal utilizará un modelo de predicción lineal utilizando filtros de Wiener

$$R_x w = r$$ 

Donde R_x corresponde con la matriz de coeficientes de autocorrelación de la señal $x(n)$ desde $r_x(0)$ hasta $r_x(p-1)$,  el predictor está descrito por el vector $w$ y $r$ son los coeficientes de autocorrelación  de $x(n)$  desde $r_x(1)$ hasta $r_x(p)$.


