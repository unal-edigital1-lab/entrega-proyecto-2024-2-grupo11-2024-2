[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=17802105&assignment_repo_type=AssignmentRepo)
# Entrega 1 del proyecto WP01

# Proyecto Digital 1: Sistema de Control de Puerta con Contraseña, NFC y FPGA

## Autores

- Carlos Pastor Alfonso Sanabria  
  *Ingeniería Eléctrica*  
  Universidad Nacional de Colombia  
  Bogotá, Colombia  
  calfonsos@unal.edu.co  

- Santiago León Naranjo  
  *Ingeniería Electrónica*  
  Universidad Nacional de Colombia  
  Bogotá, Colombia  
  saleonn@unal.edu.co  

- zBryan Daniel Marchan Castr  
  *Ingeniería Eléctrica*  
  Universidad Nacional de Colombia  
  Bogotá, Colombia  
  bmarchan@unal.edu.co  

---

## Propuesta de Proyecto: Sistema de Control de Puerta con Contraseña, NFC y FPGA

### Introducción

Este proyecto busca implementar un Sistema de Control de Puerta utilizando tecnologías avanzadas como FPGA y combinándolas con módulos de acceso moderno:  
1. Validación de contraseñas mediante un teclado matricial.  
2. Uso de un módulo NFC para la autenticación mediante tarjetas inteligentes.  
3. Visualización del estado del sistema en un display LCD (16x2).  
4. Implementación y simulación del diseño digital usando Quartus Prime y la tarjeta FPGA **Altera Cyclone IV EP4CE10E22C8**.  

El proyecto combina conceptos de Electrónica Digital, diseño en hardware (FPGA) y tecnologías modernas, orientado al diseño de sistemas de acceso controlado y seguro.

---

## Objetivo General

Diseñar e implementar un sistema electrónico de control de acceso que permita abrir una puerta mediante:  
1. La validación de una tarjeta NFC.  
2. La introducción correcta de una contraseña.  

El sistema será implementado en una FPGA y validado mediante simulación y pruebas en hardware.

---

## Objetivos Específicos

1. Validación de Tarjetas NFC: Implementar el módulo NFC para permitir acceso a tarjetas previamente autorizadas.  
2. Ingreso de Contraseña: Utilizar un teclado matricial para validar contraseñas contra una clave almacenada.  
3. Indicadores Visuales:  
   - Display LCD para mostrar mensajes como "Acceso permitido", "Acceso denegado", "Sistema bloqueado".  
   - LEDs (verde para acceso permitido, rojo para denegado).  
4. Sistema de Bloqueo:  
   - Bloquear el sistema tras tres intentos fallidos consecutivos.  
   - Activar una alarma sonora (zumbador).  
5. Uso de FPGA Diseñar el sistema lógico y de control en la FPGA Cyclone IV mediante Quartus Prime.  
6. Reinicio Manual: Incluir un botón para reiniciar el sistema tras el bloqueo.  
7. Simulación y Validación: Probar el diseño mediante simulación en Quartus Prime y pruebas físicas en la FPGA.

---

## Justificación

El control de acceso es una necesidad crítica en aplicaciones de seguridad. Este proyecto aborda la problemática combinando tecnologías modernas como NFC y LCD con el diseño de hardware digital en FPGA, brindando una solución robusta y altamente personalizable. El uso de la FPGA Cyclone IV permite a los estudiantes adquirir experiencia en diseño digital y lenguajes de descripción de hardware (VHDL o Verilog).

---

## Descripción del Proyecto

### 1. Entrada de Contraseña
- Teclado matricial (4x4) para ingresar la contraseña.  
- Verificación de la clave mediante lógica implementada en la FPGA.  

### 2. Validación NFC
- Módulo NFC (PN532 o RC522) para autenticar tarjetas mediante su ID único.  
- Lista de IDs autorizados almacenada en la FPGA o en una memoria externa conectada.  

### 3. Indicadores Visuales
- Pantalla LCD (16x2) para mostrar mensajes en tiempo real:  
  - "Acceso permitido"  
  - "Acceso denegado"  
  - "Sistema bloqueado".  
- LEDs (verde para acceso permitido, rojo para denegado).  

### 4. Sistema de Bloqueo
- Contador digital diseñado en la FPGA para registrar intentos fallidos consecutivos.  
- Activación de un zumbador tras tres intentos fallidos.  

### 5. Restablecimiento
- Botón físico conectado a la FPGA para reiniciar el sistema tras el bloqueo.

### 6. Simulación y Validación
- Simulación del diseño en Quartus Prime para validar la lógica.  
- Programación de la FPGA Cyclone IV para realizar pruebas en hardware.

---

## Materiales y Herramientas

### Hardware
- Tarjeta FPGA: **Altera Cyclone IV EP4CE10E22C8**.  
- Módulo NFC: PN532 o RC522.  
- Teclado matricial: 4x4 o 3x4.  
- Display LCD: 16x2 con módulo I2C.  
- LEDs (rojo y verde), resistencias, zumbador, botones, protoboard, cables.  
- Fuente de alimentación de 5V.  
- Programador USB Blaster para la FPGA.  

### Software
- Quartus Prime (versión Lite o Professional).  
- Arduino IDE (para programar el módulo NFC y el teclado, si es necesario).  
- Simuladores adicionales (Proteus, ModelSim).  

---

## Cronograma

| Actividad                | Duración     | Fecha Estimada     |
|--------------------------|--------------|--------------------|
| Investigación y diseño   | 1 semana     | DD/MM/AAAA         |
| Desarrollo en Quartus    | 2 semanas    | DD/MM/AAAA         |
| Simulación del circuito  | 1 semana     | DD/MM/AAAA         |
| Ensamblaje en protoboard | 2 semanas    | DD/MM/AAAA         |
| Pruebas y ajustes finales| 1 semana     | DD/MM/AAAA         |
| Elaboración del informe  | 1 semana     | DD/MM/AAAA         |

---

## Resultados Esperados

1. Validación correcta de tarjetas NFC autorizadas.  
2. Validación de contraseñas mediante teclado matricial.  
3. Indicadores funcionales (LCD, LEDs, zumbador).  
4. Sistema de bloqueo operativo tras tres intentos fallidos.  
5. Diseño funcional implementado y probado en la FPGA Cyclone IV.  
6. Capacidad de reiniciar el sistema manualmente tras un bloqueo.  

---

## Conclusión

El Sistema de Control de Puerta con Contraseña, NFC y FPGA es un proyecto educativo que combina teoría y práctica. Este proyecto permite consolidar conocimientos de electrónica digital, programación de microcontroladores, diseño con FPGAs y lenguajes de descripción de hardware, aplicados a una solución de seguridad realista y funcional.

---
