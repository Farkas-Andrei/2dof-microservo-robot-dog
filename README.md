# Robot Dog — 8× SG90, 2 DOF per leg

A small quadruped built from 8 SG90 micro servos, two per leg (hip  + knee). An MPU-6500 handles tilt sensing, and the frame is 3D-printed .
I try to keep the cost as low as possible while getting as many features as possible.
<img width="600" height="323" alt="Screenshot 2026-11-16 213211" src="https://github.com/user-attachments/assets/b88e6f82-b480-4b50-b44e-5da16d6a791b" />
<img width="707" height="477" alt="Screenshot 2026-11-16 213150" src="https://github.com/user-attachments/assets/5b41d45f-2df1-40c7-a7e9-802cd6f79486" />
<img width="621" height="280" alt="Screenshot 2026-11-16 212755" src="https://github.com/user-attachments/assets/f166a7e3-508c-4ec4-85fc-95edd000bb2c" />



## How it works

Each leg has two joints, so I can place the foot anywhere in a vertical plane by solving for the hip and knee angles from a target position. The walking pattern moves one leg at a time and shifts the body to keep the centre of mass over the supporting legs.

Power comes from a 5V buck converter for the eight servos and the controller, and a 3.3V regulator for the MPU-6500. A small voltage display sits across the battery so I can see when it sags.
(Electronics scheme along with the finish cad will arrive soon, the parts list is should be finished)
| Part | Quantity | Price (total) | Link | Notes |
| :--- | :---: | ---: | :--- | :--- |
| SG90 micro servo | 8 | €15.00 | [SigmaNortec](https://sigmanortec.ro/Servomotor-SG90-limit-switch-p141662062) | |
| MPU-6500 IMU module | 1 | €2.50 | [SigmaNortec](https://sigmanortec.ro/Modul-Accelerometru-Giroscop-I2C-MPU-6500-6-axe-p136248782) |  |
| ESP32 | 1 | €6.50 | [SigmaNortec](https://sigmanortec.ro/Placa-dezvoltare-ESP32-CH340C-4MB-WiFi-si-Bluetooth-p183799044) |  |
| 3D-printed frame (PLA) | 1 | - | - | Self-made |
| Breadboard | 1 | €1.50 | [SigmaNortec](https://sigmanortec.ro/Breadboard-400-puncte-p129872825) |  |
| 2S Li-ion battery | 1 | €6.5 | [AliExpress](https://www.aliexpress.com/item/1005005797608566.html?spm=a2g0o.order_list.order_list_main.50.724b1802llJcjF) | i don't recommend the charger bundle as mine came broken/ any s2 li-po/li-ion should work |
| 2S balance charge module | 1 | €2.00 | [SigmaNortec](https://sigmanortec.ro/modul-incarcare-litiu-2s-3s-cu-echilibrare-type-c-ridicator-tensiune) |  |
| Switch | 1 | €0.50 | [SigmaNortec](https://sigmanortec.ro/intrerupator-kcd-1-spst-onoff-23mm) |  |
| PCA9685 | 1 | €6.00 | [SigmaNortec](https://sigmanortec.ro/Modul-PCA9685-interfata-I2C-16-CH-servo-motor-p126016016) |  |
| AMS1117-3.3V | 1 | €0.80 | [SigmaNortec](https://sigmanortec.ro/Modul-coborator-tensiune-AMS1117-3-3V-p134573098) |  |
| LM2596 | 1 | €3.00 | [SigmaNortec](https://sigmanortec.ro/Modul-coborator-tensiune-reglabil-cu-display-LM2596-p134561747) |  |
| XT30 connectors | 1 male, 2 female | €1.50 | - | s |
| Breadboard and Dupont wires | - | - | - | - |
| Voltage display | 1 | €1.80 | [SigmaNortec](https://sigmanortec.ro/voltmetru-digital-028-0-100vdc-3-fire-albastru) |  |



[SigmaNortec](https://sigmanortec.ro/en/) has free delivery in Romania via EasyBox on any order over 130 lei (about 25 euro)
The delivery fee for the battery is about 10€ but it might get put back in the choice (cheap/free shipping) section
Total cost: €47.60 (excluding [AliExpres](https://www.aliexpress.com/?spm=a2g0o.order_list.logo.1.724b1802llJcjF) delivery fee)
