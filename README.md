# Robot Dog — 8× SG90, 2 DOF per leg

A small quadruped built from 8 SG90 micro servos, two per leg (hip  + knee). An MPU-6500 handles tilt sensing, and the frame is 3D-printed .
<img width="526" height="407" alt="Screenshot 2026-11-13 232547" src="https://github.com/user-attachments/assets/0aaf68fb-fe19-4255-b963-06209b137a0d" />
<img width="441" height="297" alt="Screenshot 2026-11-13 232516" src="https://github.com/user-attachments/assets/c7522354-0c76-46f4-a816-20dec3af151c" />
<img width="302" height="476" alt="Screenshot 2026-11-13 232536" src="https://github.com/user-attachments/assets/21685fe9-17d4-4ad7-9dc1-8afbd6c54c5e" />
<img width="563" height="267" alt="Screenshot 2026-11-13 232525" src="https://github.com/user-attachments/assets/4467e87f-11af-4c31-b217-2b4fd3486f11" />


## How it works

Each leg has two joints, so I can place the foot anywhere in a vertical plane by solving for the hip and knee angles from a target position. The walking pattern moves one leg at a time and shifts the body to keep the centre of mass over the supporting legs.

Power comes from a 5V buck converter for the eight servos and the controller, and a 3.3V regulator for the MPU-6500. A small voltage display sits across the battery so I can see when it sags.
