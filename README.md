
# Informe del Proyecto: Sensor DHT11 con FPGA BlackIceMX




## Introducción

Este proyecto tiene como objetivo la implementación de un sistema para la medición de temperatura ambiental utilizando la FPGA **BlackIceMX** de **Mystorm**. El sistema interactúa con el sensor **DHT11** para leer la temperatura, procesa los datos a través de un diseño realizado en **Verilog** y los muestra en dos displays de siete segmentos. Además, se implementa un sistema de alerta que envía una notificación a través de un **ESP32** cuando la temperatura alcanza un valor predefinido (27°C).

Este tipo de sistemas embebidos es fundamental en aplicaciones de **Internet de las Cosas (IoT)**, donde es necesario medir, controlar y monitorear condiciones físicas de forma remota, lo cual tiene aplicaciones en áreas como la automatización del hogar y la industria.



## Objetivos

El objetivo principal de este proyecto es diseñar y desarrollar un sistema basado en FPGA que sea capaz de realizar lo siguiente:

- Leer la temperatura ambiental a través del **sensor DHT11**.
- Mostrar la temperatura en dos displays de siete segmentos.
- Enviar una alerta a través de un módulo **ESP32** cuando la temperatura alcance un umbral predefinido (27°C).

Este sistema tiene como finalidad integrar los conocimientos adquiridos en la materia Digital 1 y aplicar conceptos de diseño en Verilog, programación en FPGA y control de periféricos como el sensor DHT11 y los displays de 7 segmentos.
 

## Componentes Utilizados

Los componentes clave utilizados en este proyecto son:

- **FPGA BlackIceMX**: Plataforma de desarrollo basada en la FPGA **Ice40HX4K** de **Lattice Semiconductor**. Se utilizó para implementar el sistema digital y manejar la entrada y salida de datos.
- **Sensor DHT11**: Sensor digital utilizado para medir la temperatura ambiental. Aunque el DHT11 también proporciona datos sobre la humedad, en este proyecto solo se utiliza la lectura de temperatura.
- **Displays de 7 segmentos**: Se utilizaron dos displays de 7 segmentos para mostrar la temperatura de manera visual. Cada display muestra un dígito de la temperatura medida. El sistema está configurado para usar un multiplexado simple para mostrar los dos dígitos.
- **ESP32**: Módulo de comunicaciones inalámbricas (WiFi y Bluetooth) que se utilizará para enviar una alerta cuando la temperatura exceda un umbral predefinido *(27°)*.

## Herramientas y Lenguajes Utilizados

- **Lenguaje de Descripción de Hardware (HDL): Verilog** fue utilizado para diseñar el sistema digital en la FPGA, permitiendo leer los datos del sensor, procesarlos y mostrarlos en los displays.
-	**Herramientas de Simulación:** Se utilizó **Xilinx ISE (XLT Lite)** para simular y verificar el comportamiento del sistema antes de implementarlo en la FPGA.
-   **IDE y Entorno de Desarrollo:** El proyecto fue desarrollado en el entorno adecuado para la FPGA BlackIceMX, que incluye herramientas para la síntesis y la carga del diseño en la FPGA.
## Descripción del Proyecto

Este proyecto consiste en la implementación de un sistema basado en FPGA que interactúa con un sensor **DHT11** para obtener la temperatura. A continuación se detallan los pasos involucrados en el sistema:

### Lectura de la Temperatura

El sensor **DHT11** envía datos de temperatura en formato digital. Estos datos son leídos por la FPGA mediante un proceso de temporización que captura la señal digital del sensor. La FPGA está diseñada para interpretar correctamente los datos del sensor y extraer el valor de temperatura.

### Procesamiento en Verilog

El diseño en **Verilog** permite procesar los datos obtenidos del sensor. El código en Verilog se encarga de gestionar las señales del **DHT11**, decodificar la información de la temperatura y luego convertirla en un formato adecuado para su visualización.

### Visualización en Displays de 7 Segmentos

Una vez que la temperatura es procesada por la FPGA, el siguiente paso es mostrarla en los displays de 7 segmentos. Cada display muestra un dígito de la temperatura medida. El código en Verilog controla el encendido y apagado de los segmentos del display para representar los dígitos de la temperatura.

### Envío de Alerta con ESP32

Cuando la temperatura alcanza un valor crítico, el sistema activa un módulo **ESP32**, que envía una alerta a través de WiFi a un servidor o a una aplicación en línea. Esto se logra mediante un diseño de comunicación entre la FPGA y el **ESP32**, donde la FPGA comunica el valor de la temperatura al **ESP32**, que posteriormente transmite la alerta.

## Diagrama de Conexión

*Aquí puedes agregar el diagrama de conexiones de la FPGA, DHT11 y displays de 7 segmentos:*

![Diagrama de Conexión](ruta/a/tu/diagrama.png)
## Resultados Esperados

- **Medición precisa de temperatura**: El sistema debe ser capaz de leer correctamente la temperatura del **DHT11**.
- **Visualización correcta**: La temperatura debe ser mostrada en los dos displays de 7 segmentos.
- **Alerta remota**: Al llegar a una temperatura específica, el sistema debe ser capaz de enviar una alerta a través de la conexión con el **ESP32**, que a su vez enviará la información a un servidor en línea.
## Conclusión

Este proyecto permite integrar varios conceptos fundamentales de electrónica digital, FPGA y sistemas embebidos. Al combinar la lectura de un sensor, el procesamiento de datos en una FPGA y la comunicación inalámbrica con un ESP32, el proyecto cubre una amplia gama de habilidades necesarias en proyectos de ingeniería electrónica.

El éxito de este proyecto dependerá de la correcta implementación y simulación del diseño en Verilog, así como de la configuración adecuada de los componentes electrónicos. Una vez implementado, el sistema será capaz de medir la temperatura de manera eficiente y enviar alertas a través de internet en tiempo real, mejorando las capacidades de monitoreo remoto en tiempo real.

## Referencias
