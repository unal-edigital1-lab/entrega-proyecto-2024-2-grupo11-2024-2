[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=17802105&assignment_repo_type=AssignmentRepo)
# Entrega 1 del proyecto WP01


# Proyecto Digital 1

## Autores
**Carlos Pastor Alfonso Sanabria**  
*Ing. Eléctrica*  
Universidad Nacional de Colombia  
Bogotá, Colombia  
calfonsos@unal.edu.co  

**Santiago León Naranjo**  
*Ing. Electrónica*  
Universidad Nacional de Colombia  
Bogotá, Colombia  
saleonn@unal.edu.co  

**Bryan Daniel Marchan Castro**  
*Ing. Eléctrica*  
Universidad Nacional de Colombia  
Bogotá, Colombia  
bmarchan@unal.edu.co  

---

## Propuesta de Proyecto: Sistema de Control de Puerta con Contraseña

### Introducción
El presente documento describe la propuesta para el desarrollo de un proyecto denominado **"Sistema de Control de Puerta con Contraseña"**. Este proyecto se enmarca en los conceptos de Electrónica Digital 1 y tiene como objetivo implementar un circuito electrónico que simule un sistema de acceso controlado mediante una contraseña digital.

---

### Objetivo General
Diseñar y construir un sistema electrónico de control de acceso que permita abrir una puerta solo al ingresar una combinación correcta de bits (contraseña).

---

### Objetivos Específicos
1. Implementar un circuito utilizando compuertas lógicas básicas (AND, OR, NOT) para procesar la contraseña.
2. Diseñar un mecanismo que indique acceso permitido (LED verde) o denegado (LED rojo).
3. Integrar un sistema de bloqueo que active una alarma si se ingresa una contraseña incorrecta en tres intentos consecutivos.
4. Presentar el diseño en simulador y en protoboard para su validación.

---

### Justificación
Este proyecto es relevante porque aborda el diseño de sistemas de control de acceso, una aplicación común en la electrónica digital moderna. A través de su implementación, se refuerzan conceptos fundamentales como el diseño lógico, el uso de flip-flops y la integración de compuertas lógicas.

---

### Descripción del Proyecto
El sistema propuesto consta de los siguientes componentes y funcionalidades:

1. **Entrada de Contraseña**  
   - Se utilizarán interruptores como entradas para representar los bits de la contraseña (combinación binaria).

2. **Validación de Contraseña**  
   - Un conjunto de compuertas lógicas verificará si la combinación ingresada coincide con la contraseña predeterminada.

3. **Indicadores**  
   - LED verde: acceso permitido.  
   - LED rojo: acceso denegado.

4. **Sistema de Bloqueo**  
   - Un contador binario y un flip-flop bloquearán el acceso tras tres intentos fallidos consecutivos, activando un zumbador como alarma.

5. **Restablecimiento**  
   - Un botón permitirá reiniciar el sistema tras el bloqueo.

---

### Materiales y Herramientas
- Compuertas lógicas integradas (ICs 7400, 7402, 7404, 7408, 7432).
- Flip-flops (IC 7474 o similar).
- Contador binario (IC 7493 o similar).
- LEDs (rojo y verde).
- Resistencias y botones.
- Zumbador.
- Protoboard y cables.
- Fuente de alimentación.
- Software de simulación (Quartus).

---

### Cronograma

| Actividad                   | Duración   | Fecha Estimada |
|-----------------------------|------------|----------------|
| Diseño del circuito         | 11 semana   | DD/MM/AAAA     |
| Simulación del sistema      | 12 semana   | DD/MM/AAAA     |
| Ensamblaje en protoboard    | 13 semanas  | DD/MM/AAAA     |
| Pruebas y ajustes finales   | 14 semana   | DD/MM/AAAA     |
| Elaboración del informe     | 15 semana   | DD/MM/AAAA     |

---

### Resultados Esperados
1. El sistema debe validar correctamente la contraseña y mostrar el estado del acceso mediante los LEDs.
2. El sistema de bloqueo debe activarse tras tres intentos fallidos y generar una alarma sonora.
3. Debe ser posible reiniciar el sistema después del bloqueo.

---

### Conclusión
El **"Sistema de Control de Puerta con Contraseña"** es un proyecto educativo que permite aplicar y consolidar los conocimientos adquiridos en Electrónica Digital 1. Su implementación refuerza habilidades de diseño lógico, uso de componentes digitales y resolución de problemas.
