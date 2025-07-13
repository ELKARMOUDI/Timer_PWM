# STM32F411 Nucleo PWM Generation

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![PWM](https://img.shields.io/badge/TIM2-PWM-green)

![C8F50C17-F0E7-4C1D-9F11-132EC0539145](https://github.com/user-attachments/assets/2895ed35-e3ea-4672-b693-aa93f7af12a2)



Generate PWM signals using TIM2 on STM32F411 Nucleo board.

## Features
- **Adjustable PWM** on TIM2_CH1 (PA5)
- **2Hz Base Frequency** (configurable)
- **0-100% Duty Cycle** (initial 0%)
- **64MHz System Clock** (HSI-based PLL)
- **HAL Implementation**

## Hardware Configuration
| Component | Specification | Nucleo Reference |
|-----------|---------------|------------------|
| MCU       | STM32F411RE   | MB1136 User Manual |
| PWM Pin   |  PA5          | Check board schematic |
| Clock     | HSI 16MHz     | Internal |

## Technical Details
### Clock Tree 
```c
HSI (16MHz) → PLL → 64MHz SYSCLK
PLLM = 8, PLLN = 64, PLLP = 2
APB1 Prescaler = 2 → TIM2 Clock = 32MHz
