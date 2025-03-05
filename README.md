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

| Actividad                | Duración Semana| Fecha Estimada     |
|--------------------------|----------------|--------------------|
| Investigación y diseño   |       10       | 24/01/2025         |
| Desarrollo en Quartus    |       11       | 28/01/2025         |
| Simulación del circuito  |       12       | 04/02/2025         |
| Ensamblaje en protoboard |       13       | 11/02/2025         |
| Pruebas y ajustes finales|       14       | 18/02/2025         |
| Elaboración del informe  |       15       | 25/02/2025         |

---

## Resultados Esperados

1. Validación correcta de tarjetas NFC autorizadas.  
2. Validación de contraseñas mediante teclado matricial.  
3. Indicadores funcionales (LCD, LEDs, zumbador).  
4. Sistema de bloqueo operativo tras tres intentos fallidos.  
5. Diseño funcional implementado y probado en la FPGA Cyclone IV.  
6. Capacidad de reiniciar el sistema manualmente tras un bloqueo.  

---

## Teclado Matricial 
El modulo de teclado recorre las filas del teclado matricial activando una por una, para hacerlo creamos un contador que cambia con cada flanco de reloj, como son cuatro filas creamos el contador de dos bits para asi tener las cuatro posibles combinaciones, si se presiona una tecla la columna cerrara el circuito y mediante esta combinacion de fila y columna encendidas podemos identificar la tecla presionada. Cuando identificamos la tecla presionada enviamos una salida con el binario de la tecla correspondiente. 

```verilog
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

Entity teclado_7seg is
PORT (
        Reloj     : in  std_logic;
        col       : in  STD_LOGIC_VECTOR (3 downto 0);
        filas     : out STD_LOGIC_VECTOR (3 downto 0);
        display   : out STD_LOGIC;
        Segmentos : out STD_LOGIC_VECTOR (7 downto 0)
    );
end teclado_7seg;

architecture TecladoMatricial of teclado_7seg is

component LIB_TEC_MATRICIAL_4x4_INTESC_RevA is
        GENERIC (
            FREQ_CLK : INTEGER := 50000000
        );
		  
Port (
    CLK        : in  STD_LOGIC;
    COLUMNAS   : in  STD_LOGIC_VECTOR (3 downto 0);
    FILAS      : out STD_LOGIC_VECTOR (3 downto 0);
    BOTON_PRES : out STD_LOGIC_VECTOR (3 downto 0);
    IND        : out STD_LOGIC
);
end component LIB_TEC_MATRICIAL_4x4_INTESC_RevA;

SIGNAL boton_pres: STD_LOGIC_VECTOR (3 downto 0); -- Señal para almacenar el botón presionado
SIGNAL ind : STD_LOGIC; -- Señal para indicar si se ha presionado un botón
SIGNAL segm : STD_LOGIC_VECTOR (7 downto 0) := "00000000"; -- Señal para los segmentos del display

begin

libreria : LIB_TEC_MATRICIAL_4x4_INTESC_RevA  
    Generic map (FREQ_CLK => 50000000)
    Port map (Reloj, col, filas, boton_pres, ind);

Proceso_teclado_7seg: process (Reloj) -- Eliminado boton_pres_segm
begin
    if rising_edge (Reloj) then
        if ind = '1' then
            case boton_pres is
                when "0000" => segm <= "11000000"; -- 0
                when "0001" => segm <= "11111001"; -- 1
                when "0010" => segm <= "10100100"; -- 2
                when "0011" => segm <= "10110000"; -- 3
                when "0100" => segm <= "10011001"; -- 4
                when "0101" => segm <= "10010010"; -- 5
                when "0110" => segm <= "10000010"; -- 6
                when "0111" => segm <= "11111000"; -- 7
                when "1000" => segm <= "10000000"; -- 8
                when "1001" => segm <= "10011000"; -- 9
                when "1010" => segm <= "10001000"; -- A
                when "1011" => segm <= "10000011"; -- B
                when "1100" => segm <= "11000110"; -- C
                when "1101" => segm <= "10100001"; -- D
                when "1110" => segm <= "10000110"; -- E
                when "1111" => segm <= "10001110"; -- F
                when others => segm <= "11111111"; -- Apagar display en caso de error
            end case;
        end if;
    end if;
end process;

display <= '0'; -- Asignación de valor a la salida display
Segmentos <= segm; -- Asignación de la señal a la salida Segmentos

end TecladoMatricial;
```
Asignacion de pines:
* ![pines](https://github.com/unal-edigital1-lab/entrega-proyecto-2024-2-grupo11-2024-2/blob/main/WhatsApp%20Image%202025-03-04%20at%2011.34.59%20PM.jpeg)

[video funcionamiento](https://drive.google.com/file/d/17z23vGBHdEPNfBG5SV9F3vzCaU1XL8vD/view?usp=sharing)

## Pantalla LCD 
El modulo de pantalla nos permite visualizar los estados tras la comparacion de los digitos ingresados con el teclado matricial y la contraseña predeterminada.
```verilog
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;
USE WORK.COMANDOS_LCD_REVD.ALL;

entity LIB_LCD_INTESC_REVD is
GENERIC(
    FPGA_CLK : INTEGER := 100_000_000
);

PORT(
    CLK: IN STD_LOGIC;
    -- PUERTOS DE LA LCD
    RS : OUT STD_LOGIC;
    RW : OUT STD_LOGIC;
    ENA : OUT STD_LOGIC;
    DATA_LCD : OUT STD_LOGIC_VECTOR(7 DOWNTO 0)
);

end LIB_LCD_INTESC_REVD;

architecture Behavioral of LIB_LCD_INTESC_REVD is

CONSTANT NUM_INSTRUCCIONES : INTEGER := 12;

-- COMPONENTES Y SEÑALES PARA LCD
component PROCESADOR_LCD_REVD is
GENERIC(
    FPGA_CLK : INTEGER := 50_000_000;
    NUM_INST : INTEGER := 1
);
PORT(
    CLK : IN STD_LOGIC;
    VECTOR_MEM : IN STD_LOGIC_VECTOR(8 DOWNTO 0);
    C1A,C2A,C3A,C4A : IN STD_LOGIC_VECTOR(39 DOWNTO 0);
    C5A,C6A,C7A,C8A : IN STD_LOGIC_VECTOR(39 DOWNTO 0);
    RS : OUT STD_LOGIC;
    RW : OUT STD_LOGIC;
    ENA : OUT STD_LOGIC;
    BD_LCD : OUT STD_LOGIC_VECTOR(7 DOWNTO 0);
    DATA : OUT STD_LOGIC_VECTOR(7 DOWNTO 0);
    DIR_MEM : OUT INTEGER RANGE 0 TO NUM_INSTRUCCIONES
);
end component PROCESADOR_LCD_REVD;

COMPONENT CARACTERES_ESPECIALES_REVD is
PORT(
    C1,C2,C3,C4 : OUT STD_LOGIC_VECTOR(39 DOWNTO 0);
    C5,C6,C7,C8 : OUT STD_LOGIC_VECTOR(39 DOWNTO 0)
);
end COMPONENT CARACTERES_ESPECIALES_REVD;

type ram is array (0 to NUM_INSTRUCCIONES) of std_logic_vector(8 downto 0);
signal INST : ram := (others => (others => '0'));
signal blcd : std_logic_vector(7 downto 0):= (others => '0');
signal vector_mem : STD_LOGIC_VECTOR(8 DOWNTO 0) := (others => '0');
signal c1s,c2s,c3s,c4s : std_logic_vector(39 DOWNTO 0) := (others => '0');
signal c5s,c6s,c7s,c8s : std_logic_vector(39 DOWNTO 0) := (others => '0');
signal dir_mem : integer range 0 to NUM_INSTRUCCIONES := 0;

begin

-- INSTANCIACIÓN DE COMPONENTES
u1: PROCESADOR_LCD_REVD
GENERIC map( FPGA_CLK => FPGA_CLK, NUM_INST => NUM_INSTRUCCIONES )
PORT map( CLK, VECTOR_MEM, C1S, C2S, C3S, C4S, C5S, C6S, C7S, C8S, RS, RW, ENA, BLCD, DATA_LCD, DIR_MEM );

U2 : CARACTERES_ESPECIALES_REVD
PORT MAP( C1S, C2S, C3S, C4S, C5S, C6S, C7S, C8S );

VECTOR_MEM <= INST(DIR_MEM);

-- INSTRUCCIONES PARA ESCRIBIR "HOLA MUNDO" EN LA LCD
INST(0) <= LCD_INI("11"); -- Inicializamos LCD
INST(1) <= POS(1,1); -- Cursor en línea 1, columna 1
INST(2) <= CHAR(MP);
INST(3) <= CHAR(R);
INST(4) <= CHAR(O);
INST(5) <= CHAR(Y);
INST(6) <= CHAR(E); -- Espacio
INST(7) <= CHAR(C);
INST(8) <= CHAR(T);
INST(9) <= CHAR(O);
INST(10) <= CHAR_ASCII(X"20"); -- Espacio
INST(11) <= CHAR(a);
INST(12) <= CODIGO_FIN(1); -- Finalizamos

end Behavioral;
```
* ![pines](https://github.com/unal-edigital1-lab/entrega-proyecto-2024-2-grupo11-2024-2/blob/main/2.jpeg)

[video funcionamiento](https://drive.google.com/file/d/1815cJtCKZybjZDVTcco8qGg2A90Iz54p/view?usp=sharing)



## Conclusión

El Sistema de Control de Puerta con Contraseña, NFC y FPGA es un proyecto educativo que combina teoría y práctica. Este proyecto permite consolidar conocimientos de electrónica digital, programación de microcontroladores, diseño con FPGAs y lenguajes de descripción de hardware, aplicados a una solución de seguridad realista y funcional.

---
