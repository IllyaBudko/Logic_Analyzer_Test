# Logic_Analyzer_Test

This is a simple project to test a logic analyzer for STM32F4DISCOVERY board.

Connections to be made from logic analyser to the board:

MCO1:
(master clock output 1, any logic analyzer channel can be used)
  - pin PA8, MCO1

UART:
(uart rx only, any logic analysed channel can be used)
  - pin PA2, UART TX

SPI:
(any 2 analyzer channels can be used as long as they are next to each other, to be able to see data and clk 
in relation to each other)
  - pin PA5, SPI CLK
  - pin PA7, SPI DATA
  
Operation:
Simple loop in main that transmits string "Hello World! This string is to test Logic Analyzer channels."
with SPI and UART in polling mode. MCO1 always outputs independantly of code.

Binary and ELF files are in debug folder.

Thats about it.
