**Industrial-Pick-and-Place-Robot-with-BLE-Control-and-Vision-Integration**

# **Project Objective:**

Designed and built a BLE-enabled industrial pick-and-place robot capable of identifying, grasping, and relocating objects placed at varying heights. The system integrates computer vision for object detection, ultrasonic sensors for obstacle avoidance, and a rack-and-pinion mechanism for vertical motion, all coordinated through an Arduino Mega-based control stack.

# **Project Overview:**

Industrial pick-and-place automation requires dynamic adaptability across height levels and spatial constraints. This project delivers a robust mobile robotic arm capable of real-time visual identification and precise actuation in a semi-structured environment. The robot’s BLE remote-control interface, coupled with sensor-guided decision-making and mechanical lifting, enables responsive manipulation tasks ideal for modern factory floors.

The project includes:

- **Mobile Base:** For navigating the robot in constrained spaces.
- **Rack-and-Pinion Lift System:** For lifting the gripper to various vertical levels.
- **2-DOF Gripper Arm:** For actuating the end-effector to grasp objects of different shapes and sizes.

# **Key Contributions:**

- **Vision-Based Object Detection:** Integrated a camera module with OpenCV running on a companion processor to detect target objects and trigger pick actions based on size and color.
- **BLE Remote Control:** Developed a BLE-based communication pipeline allowing remote control via a custom Android app, enabling flexible task delegation and user interaction.
- **Obstacle Avoidance System:** Placed ultrasonic sensors on the robot’s sides to detect surrounding objects, dynamically halting movement in case of proximity threats.
- **Precision Pick-and-Lift:** Implemented a rack-and-pinion drive for height adjustments and a 2-DOF DC-motor-driven gripper, enabling payload handling over variable elevations.

# **Methodology:**

**1. Mechanical Design:**

- CAD model of dual-level robot chassis and rack assembly designed in Fusion 360.
- Designed gripper assembly with 2 degrees of freedom and mechanically coupled fingers actuated via DC motors.

**2. Embedded Systems:**

- Programmed the Arduino Mega to control motion, BLE interface, and sensor feedback loops.
- Integrated ultrasonic sensors for continuous obstacle monitoring during navigation and arm extension.

**3. Computer Vision Pipeline:**

- Implemented an OpenCV-based object detection algorithm for color- and shape-based recognition.
- Synchronized vision-based decision logic with actuator commands for closed-loop task execution.

# **Challenges and Solutions:**

- **Unstable Grip at Varying Heights:** Introduced torque-compensated lift delays and PID-based gripper stabilization to improve precision.
- **Sensor Interference:** Isolated BLE communication from ultrasonic signal spikes using hardware filtering.
- **Latency in BLE Response:** Optimized BLE command parsing and added a basic queue handler to smooth transitions.

# **Key Outcomes:**

- Successfully picked and placed objects across 3 height levels with ≤5° end-effector drift.
- Maintained obstacle avoidance within a 15 cm buffer zone using ultrasonic proximity sensing.
- Enabled modular BLE remote operations with user-controlled override and task queuing.

# **Technologies and Tools:**

- **Controller:** Arduino Mega
- **Sensors:** Ultrasonic proximity sensors, BLE module, camera
- **Mechanisms:** Rack and pinion, 2-DOF DC motor gripper
- **Software Stack:** C/C++ (Arduino), OpenCV (vision), MIT App Inventor (BLE app)
- **CAD & Fabrication:** Fusion 360, 3D printing, acrylic chassis, aluminum rails

# **Future Improvements:**

- Replace BLE with Wi-Fi/MQTT for improved communication latency and scalability.
- Add inverse kinematics to allow multi-point pick path planning.
- Expand the CV pipeline to detect object orientation for more robust grip planning.

This system demonstrates an integrated approach to low-cost industrial automation, blending mechatronic design, perception, and embedded control for real-world manipulation tasks.
