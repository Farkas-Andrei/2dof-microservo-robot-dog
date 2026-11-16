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
