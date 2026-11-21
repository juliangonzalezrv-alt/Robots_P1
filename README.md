# Project-01-Robots-G4: Robot Móvil Ackermann (Dodge Challenger)

Diseño CAD en **Autodesk Fusion 360**, exportación **URDF/Xacro**, simulación en **Gazebo** y controlador de trayectoria en **ROS 2**.

## Estructura del Repositorio

- `ackermann_challenger_description/`: Modelo URDF/Xacro, mallas `.stl` y archivos de lanzamiento para visualización y simulación.
- `ackermann_challenger_control/`: Controlador Ackermann, generador de trayectoria, mundos de Gazebo y configuración (`ros2_control`).
- `cad/`: Archivo fuente de Fusion 360 (`.f3d`), planos acotados en PDF y capturas/renders del robot.
- `docs/`: Documento técnico en formato IEEE y presentación del proyecto.

## Parámetros de Diseño (Escala 1:10)

| Parámetro | Valor |
| :--- | :---: |
| Distancia entre ejes (*Wheelbase*, $L$) | `0.300 m` (`300 mm`) |
| Ancho de vía (*Track Width*, $W$) | `0.190 m` (`190 mm`) |
| Separación entre pivotes (*Kingpin Width*, $W_s$) | `0.120 m` (`120 mm`) |
| Radio de rueda ($R_w$) | `0.035 m` ($\varnothing 70\text{ mm}$) |
| Ángulo máximo de dirección ($\delta_{\max}$) | $\pm 35^\circ$ (`±0.611 rad`) |

## Dependencias y Requisitos

- **ROS 2:** Humble / Jazzy
- **Simulador:** Gazebo
- **Paquetes requeridos:** *(completar con los paquetes exactos usados por el controlador, ej. `ros2_control`, `ros2_controllers`, `xacro`, `robot_state_publisher`, `ros_gz_sim` / `gazebo_ros_pkgs`)*

## Compilación y Ejecución

```bash
# Clonar dentro del workspace de ROS 2
cd ~/ros2_ws/src
git clone https://github.com/FernandoVB01/Project-01-Robots-G4.git

# Compilar
cd ~/ros2_ws
colcon build --symlink-install
source install/setup.bash

# Ejecutar simulación y trayectoria
# ros2 launch ackermann_challenger_control <nombre_launch>.launch.py
```
