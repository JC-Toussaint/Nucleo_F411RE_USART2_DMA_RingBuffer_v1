# Nucleo_F411RE_USART2_DMA_RingBuffer_v1
Nucleo F4 USART2 using DMA circular buffer

This application uses DMA in circular mode to continuously receive UART characters directly into 
a ring buffer in RAM without CPU time, the buffer size is your choice.

One simply scans this DMA buffer from the background routine and processes the incoming characters there.
One uses hdmarx->Instance->NDTR to determine where the DMA write pointer is and thus the number of characters received.
