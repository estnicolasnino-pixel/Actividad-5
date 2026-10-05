# Actividad-5
# Control en Tiempo Real de Brazo Robótico (URDF + ESP32)

Sistema de control mecatrónico en tiempo real para la simulación física 3D de un brazo robótico articulado en **PyBullet**, controlado mediante un microcontrolador **ESP32** y un **módulo Joystick analógico de 3 ejes** a través de comunicación serial UART.

---

##  Esquema de Conexiones Hardware

| Componente | Pin Joystick | Pin ESP32 | Función en Simulación |
| :--- | :--- | :--- | :--- |
| **Eje X (VRx)** | Output Analógico | `GPIO 34` (ADC) | Rotación de la Base (`joint_1`) |
| **Eje Y (VRy)** | Output Analógico | `GPIO 35` (ADC) | Inclinación del Brazo (`joint_2`) |
| **Botón (SW)** | Output Digital | `GPIO 32` (Pull-Up) | Apertura / Cierre de Pinza (`Gripper`) |
| **Alimentación** | VCC / GND | 3.3V / GND | Alimentación del módulo |

---

##  Requisitos e Instalación

### Software Requerido
* **Python 3.10+**
* **Arduino IDE 2.x** (con soporte para placas ESP32)
* **Visual Studio Code**

### Librerías de Python
Instala las dependencias necesarias ejecutando en tu terminal:
```bash
python -m pip install pybullet pyserial
