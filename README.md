# Proyecto Sensor DHT11 con FPGA BlackIceMX

Este proyecto tiene como objetivo poner en práctica los conceptos aprendidos en la materia Digital 1, utilizando la FPGA **BlackIceMX** de **Mystorm** para leer la temperatura desde el sensor **DHT11** y mostrarla en dos displays de siete segmentos. Además, se implementa un sistema de alerta que envía una notificación a través de un **ESP32** cuando la temperatura alcance un valor predeterminado.

## Objetivo

El objetivo principal de este proyecto es:

- Leer la temperatura ambiental con el **sensor DHT11**.
- Mostrar la temperatura en dos displays de siete segmentos.
- Enviar una alerta a través de un **ESP32** cuando se alcance una temperatura crítica.

## Componentes Utilizados

- **FPGA BlackIceMX**: Placa de desarrollo para implementar el diseño.
- **Sensor DHT11**: Sensor de temperatura utilizado para leer la temperatura ambiental.
- **Displays de 7 segmentos**: Para mostrar la lectura de temperatura.
- **ESP32**: Módulo para enviar la alerta al alcanzar una temperatura específica.

## Herramientas y Lenguajes Utilizados

- **Lenguaje de descripción de hardware (HDL)**: **Verilog**.
- **Herramientas de simulación**: **Xilinx ISE (XLT Lite)**.
- **IDE**: Herramientas digitales y de simulación para FPGA.

## Descripción del Proyecto

Este proyecto consiste en la implementación de un sistema basado en FPGA que interactúa con un sensor DHT11 para obtener la temperatura. A continuación, los datos obtenidos son procesados en **Verilog** y mostrados en los displays de 7 segmentos.

El sistema incluye también una alerta que es activada a través del **ESP32** cuando la temperatura alcanza el umbral predefinido. Esto permite monitorear y tomar acciones basadas en la temperatura, todo controlado por la FPGA.

## Diagrama de Conexión

*Aquí puedes agregar el diagrama de conexiones de la FPGA, DHT11 y displays de 7 segmentos:*

![Diagrama de Conexión](ruta/a/tu/diagrama.png)

## Resultados Esperados

- **Medición precisa de temperatura**: El sistema debe ser capaz de leer correctamente la temperatura del **DHT11**.
- **Visualización en displays de 7 segmentos**: La temperatura debe ser mostrada en dos displays de 7 segmentos.
- **Alerta remota**: Cuando se alcanza una temperatura crítica, el **ESP32** debe enviar una alerta a un servidor o red.

## Estructura del Proyecto

El proyecto está organizado en varias carpetas dentro del repositorio:

Sensor-DHT11-FPGA-Ice40HX4K/
├── src/ # Código fuente en Verilog
├── docs/ # Documentación adicional
├── hardware/ # Archivos de configuración de la FPGA
├── test/ # Pruebas y simulaciones
├── README.md # Descripción general del proyecto
└── LICENSE # Licencia del proyecto



## Licencia

Este proyecto está bajo la licencia **MIT**. Puedes modificar, distribuir y usar este código como desees, bajo los términos de la licencia.

---

**¡Gracias por visitar este proyecto! Si tienes alguna pregunta o sugerencia, no dudes en abrir un issue o hacer un pull request.**

