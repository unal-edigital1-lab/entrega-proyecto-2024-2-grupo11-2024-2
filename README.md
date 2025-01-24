[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=17802105&assignment_repo_type=AssignmentRepo)
# Entrega 1 del proyecto WP01

# Proyecto Digital 1: Sistema de Control de Puerta con Contraseña y NFC

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

- Bryan Daniel Marchan Castro  
  *Ingeniería Eléctrica*  
  Universidad Nacional de Colombia  
  Bogotá, Colombia  
  bmarchan@unal.edu.co  

---

## Propuesta de Proyecto: Sistema de Control de Puerta con Contraseña y NFC

### Introducción

Este proyecto busca implementar un Sistema de Control de Puerta utilizando diversas tecnologías:  
1. Validación de contraseñas mediante un teclado matricial.  
2. Uso de un módulo NFC para la autenticación mediante tarjetas inteligentes.  
3. Visualización del estado del sistema en un display LCD (16x2).  

El proyecto combina conceptos de Electrónica Digital con tecnologías modernas, orientado al diseño de sistemas de acceso controlado y seguro.

---

## Objetivo General

Diseñar e implementar un sistema electrónico de control de acceso que permita abrir una puerta mediante:  
1. La validación de una tarjeta NFC.  
2. La introducción correcta de una contraseña.  

El sistema debe incluir un mecanismo de bloqueo tras múltiples intentos fallidos y mostrar el estado en un display LCD.

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
5. Reinicio Manual: Incluir un botón para reiniciar el sistema tras el bloqueo.  
6. Simulación y Validación: Probar el diseño en simulador y protoboard.

---

## Justificación

El control de acceso es una necesidad en múltiples aplicaciones de seguridad. Este proyecto aborda esta problemática combinando tecnologías modernas (NFC y displays LCD) con fundamentos de electrónica digital, permitiendo a los estudiantes consolidar sus habilidades en diseño e implementación de sistemas electrónicos.

---

## Descripción del Proyecto

El sistema propuesto consta de los siguientes módulos:

### 1. Entrada de Contraseña
- Teclado matricial (4x4) para ingresar la contraseña.  
- Verificación de la clave mediante lógica programada en el microcontrolador.  

### 2. Validación NFC
- Módulo NFC (PN532 o RC522) para autenticar tarjetas mediante su ID único.  
- Lista de IDs autorizados almacenada en memoria.  

### 3. Indicadores Visuales
- Pantalla LCD (16x2) para mostrar mensajes en tiempo real:  
  - "Acceso permitido"  
  - "Acceso denegado"  
  - "Sistema bloqueado".  
- LEDs (verde para acceso permitido, rojo para denegado).  

### 4. Sistema de Bloqueo
- Contador para registrar intentos fallidos consecutivos.  
- Activación de un zumbador tras tres intentos fallidos.  

### 5. Restablecimiento
- Botón físico para reiniciar el sistema tras el bloqueo.

---

## Materiales y Herramientas

### Hardware
- Microcontrolador: Arduino Uno, Mega o similar.  
- Módulo NFC: PN532 o RC522.  
- Teclado matricial: 4x4 o 3x4.  
- Display LCD: 16x2 con módulo I2C.  
- LEDs (rojo y verde), resistencias, zumbador, botones, protoboard, cables.  
- Fuente de alimentación de 5V.  

### Software
- Arduino IDE.  
- Software de simulación (Quartus, Proteus o Tinkercad).  

---

## Cronograma

| Actividad                | Duración     | Fecha Estimada     |
|--------------------------|--------------|--------------------|
| Investigación y diseño   | 1 semana     | DD/MM/AAAA         |
| Programación del sistema | 2 semanas    | DD/MM/AAAA         |
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
5. Capacidad de reiniciar el sistema manualmente tras un bloqueo.  

---

## Conclusión

El Sistema de Control de Puerta con Contraseña y NFC es un proyecto educativo que combina teoría y práctica. Permite consolidar conocimientos de electrónica digital, programación de microcontroladores y diseño lógico, aplicados a una solución de seguridad realista.

---

## Licencia

Este proyecto está disponible bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.
