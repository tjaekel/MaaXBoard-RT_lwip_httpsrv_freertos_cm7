# MaaXBoard-RT_lwip_httpsrv_freertos_cm7
 MaaxBoard RT HTTP server with FreeRTOS

## 100M vs. 1G PHY
Project works (and is changed) to use the 100M PHY and connector.
The 1G is a different PHY:
modify from "golden reference" project, e.g. AVNET "out-of-box" demo.

It is the SDK project, modified for the MaaXBoard-RT, esp. the
memory regions used (it was wrong after setting project up: bss sections
was writing outside available memory regions,. BusFault_Handler was
invoked).
Fix it by checking carefully the "MCU Settings", the ememory regions used.
Best:
"Import" a working XML file on "MCU Settings".

## TODO
modify project for 1G PHY (a different one on board, as documented)

