# Lab 1: Introducción al diseño digital con HDL y herramientas EDA de síntesis
## 1. Abreviaturas y definiciones.
FPGA: Field Programmable Gate Arrays.
## 2. Referencias.

[1] Mano, M. M., & Ciletti, M. D. (2013). Diseño Digital (5a ed.). Pearson.
[2] Chu, P. P. (2008). FPGA Prototyping by SystemVerilog Examples (3a ed.). Wiley.

## 3. Desarrollo

### 3.5 Decodificador siete segmentos.

#### 1. Ideas básicas .
Se plantea usar los siguientes sistemas.

ciclador_seg        : Se encarga de generar una señal cada dos segundos que funciona como habilitador para almacenar valores en el registro.

Control             : Es el encargado de generar las señales para habilitar los segmentos según los valores de salida del banco de registros, tomando los bits de cuatro en cuatro y los ánodos.

Decodificador       : Toma los valores de salida del banco de registros y los decodifica para mostrarlos en el display de siete segmentos cada 1 ms.

LFSR                : Genera números aleatorios para almacenar en el banco de registros.

Register_bank       : Se encarga de almacenar los valores generados por el LFSR.

Top_siete_segmentos : Se realizan las conexiones de los módulos.

Top_basys_seg       : Se instancia el reloj para la FPGA y se utiliza para la síntesis.


#### 2. Testbench.

Se hicieron para vericar el comportamienta que se obtine en el sistema del site segmentos.


