# Indice Big Mac Agosto 2020 UY

La idea es poder calcular la cotización del dolar implícita en el precio de la Big Mac en diferentes países, y compararla con el tipo de cambio de mercado. La metodología se explica claramente en https://www.economist.com/news/2020/07/15/the-big-mac-index

El proyecto fue realizado en R. Se analizan los países: Argentina, Brasil, Estados Unidos, México, zona euro (Alemania, España, Italia), y se comparan con Uruguay. Los países seleccionados son los de rerefencia por el Banco Central de Uruguay para calcular el tipo de cambio real global y regional.

El precio de la Big Mac se puede consultar en páginas de delivery de otros países del mundo. 

Los paquetes utilizados fueron: 

* readxl
* tidyverse
* stringr
* knitr
* lubridate
* modelr
* tinytext
* ggrepel
* broom

También se calcula el Índice Big Mac ajustado. Para ajustar el Índice Big Mac, se realiza una regresión simple entre el precio de la Big Mac en dólares y el PIB per cápita en dólares, y se obtienen estimaciones del precio. Es posible calcular el tipo de cambio real de equilibrio según las productividades, y luego el tipo de cambio real implícito en el precio de la Big Mac. 

Si el tipo de cambio real según el precio de la Big Mac es inferior al de equilibrio, entonces la moneda del país debería depreciarse para alcanzar el equilibrio.  
