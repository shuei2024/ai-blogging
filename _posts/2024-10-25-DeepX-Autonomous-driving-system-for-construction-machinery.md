---
layout: post
title: "DeepX: Autonomous driving system for construction machinery"
date: 2024-10-25 10:00:00 +0900
author: Tri Thanh
categories: AI Engineer, AI Update
---

## Author: Tri Thanh


# DeepX: Autonomous driving system for construction machinery

## What is DeepX?

DeepX is a company with the mission to "automate all machines and revolutionize production sites around the world."

In Japan, demographic trends such as an aging population and declining birth rates are creating serious structural challenges across various industries. Globally, however, technological advancements in fields like robotics and artificial intelligence are rapidly evolving, promising solutions to these difficulties and driving further innovation. Japan, with its long-standing strengths in hardware manufacturing across a wide range of sectors, is well-positioned to leverage these advancements. The manufacturing industry remains a cornerstone of Japan's economy, and as demographic trends impact other nations similarly in the future, Japan's current challenges may serve as a model for the rest of the world.

DeepX seeks to integrate Japan's robust manufacturing capabilities with cutting-edge software technologies, following a threefold approach. First, the company aims to develop technologies that automate a diverse array of machines. Second, it focuses on addressing Japan’s pressing demographic and industrial challenges. Third, by refining these technologies, DeepX plans to expand globally, offering solutions developed through the process of tackling Japan’s issues.

The mission of "automating all machines and revolutionizing production sites worldwide" is expected to drive significant social and economic changes, not only within Japan but globally. DeepX is committed to pursuing this vision and working diligently to achieve it, believing it will spur innovation on a large scale.

## Robotics Section

DeepX has developed a realistic robotic simulation environment, leveraging ROS2 (Robot Operating System 2) to ensure system robustness and scalability. This advanced system underpins DeepX's work in autonomous driving and control technologies for heavy machinery, particularly in dynamic environments like construction sites.

### User Interface (UI) Design for Practical Use

For projects approaching on-site demonstration or deployment, DeepX designs and develops a user-friendly UI, anticipating its use by non-engineers and on-site workers. The UI is refined continuously through feedback received during trial use to ensure optimal usability and efficiency for practical applications.

## Control Section

### Path Generation and Trajectory Following

Construction sites present ever-changing conditions, making it essential for autonomous driving systems to adapt quickly. To address these challenges, DeepX has created advanced path generation and trajectory following technologies designed to work with various machines and terrains.

The path generation technology developed by DeepX covers the entire excavation process—from digging and moving soil to removal. This technology combines the expertise of experienced operators with real-time optimization algorithms to maximize excavation efficiency regardless of terrain type. During the earthmoving phase, cutting-edge motion planning algorithms ensure smooth navigation while avoiding obstacles.

The trajectory following technology deals with unpredictable factors such as hydraulic system dynamics, uneven terrain, sensor failures, and system instability. DeepX's control algorithms are designed to be resilient to these uncertainties, utilizing advanced modeling and optimization techniques grounded in extensive simulation testing. These technologies have been applied across a variety of construction sites and machines, confirming their adaptability and robustness.

### Collision Prevention

Safety is a top priority at DeepX, which is why collision prevention technologies have been integrated into both autonomous and remote operation systems.

The autonomous driving system features collision avoidance capabilities that ensure safe interaction with other remotely operated construction machinery. If necessary, the system can autonomously stop the machine to prevent collisions. In addition to this, DeepX has developed an intuitive collision avoidance system for remote operations. This system allows the machine to maintain a safe distance from obstacles, while minimally interfering with the operator’s control inputs. It removes only those components of the operator's signal that would lead to a collision, without significantly altering the overall control.

This function is powered by high-performance real-time algorithms and advanced predictive models, which estimate distances to future surrounding objects. The collision avoidance system considers all obstacles in the environment, including walls, buckets, and other moving machinery, ensuring safe and efficient operations in complex environments.

## Perception Section

### Object Detection Using Point Cloud Data

DeepX utilizes point cloud data from Lidar sensors to detect and recognize objects necessary for autonomous operation of construction machinery, such as dump trucks and earth buckets, ensuring real-time detection and response. For instance, DeepX has developed a system that processes point cloud data from Lidar to determine the relative position and posture of dump trucks as observed from a hydraulic excavator. The system also evaluates the shape of the truck's vessel and its loading status. To handle varying conditions such as different positions, postures, and soil shapes, the engineers of DeepX developed a specialized algorithm based on a deep neural network, ensuring accurate recognition in diverse environments.

### Map Creation Using Point Cloud Data

DeepX also uses point cloud data from Lidar for real-time environmental recognition and visualization around construction machinery at work sites. For example, they created a system that processes point cloud data from multiple Lidar units and other relevant sensor data to track the environment around a caisson excavator. This system also identifies the real-time position and attitude of the construction machinery itself, enabling precise and adaptive control.

## Simulation Section

### Generating Point Cloud Data with Lidar Scan Patterns

DeepX leverages simulation data to develop, train, and verify object detection models using point cloud data. Real-world Lidar data often exhibits unique scanning patterns, making simple random sampling from 3D simulation models insufficient for accurate training. To address this, DeepX reproduces specific Lidar scanning patterns in simulations, allowing for the generation of realistic Lidar data. This simulated data is then used to refine and verify object detection models and systems, ensuring they are ready for real-world application.

## Notable Use Cases

### On-site Demonstration of Continuous Autonomous Operation of Excavators

In April 2023, DeepX successfully demonstrated an autonomous hydraulic excavator system in collaboration with Fujita Corporation. This system autonomously completed repetitive cycles of excavation and dump loading at a real construction site. The demonstration marks a significant milestone in autonomous operations for heavy machinery in dynamic environments like construction sites, where conditions such as dump truck positions, soil shapes, and excavation areas continuously change.

#### Challenges in Stabilizing Complex Systems for Autonomous Operation

Achieving stable autonomous operations in such environments presents unique challenges due to the need for systems to adapt in real time to complex, changing conditions. For example, during loading, hydraulic excavators must recognize their surroundings, adjust to varying dump truck positions and orientations, and adapt to soil shape and hardness. Such complexity tends to destabilize the system, making it difficult to ensure continuous, reliable operations. Stability is a key factor for the practical implementation of autonomous machinery, especially when dealing with highly dynamic and unpredictable conditions like those at construction sites.

#### Demonstration of Continuous, Autonomous Excavation and Loading

During the demonstration at Fujita’s construction site, the autonomous system adjusted its movements based on the dump truck's specifications (e.g., position, orientation, and soil volume) and the characteristics of the excavation area. The system successfully operated for eight continuous hours, completing over 200 cycles of excavation and loading without human intervention, thus confirming both its adaptive capabilities and operational stability under real-world conditions.

#### Software Development and Integration by DeepX

The autonomous excavator system was developed using the Robot Operating System 2 (ROS2) framework. DeepX's contributions centered on software development, including perception and control algorithms, as well as simulators for testing and verification. Fujita Corporation supported the project by providing the demonstration site and the necessary hardware for testing. This collaboration highlights DeepX's role in advancing autonomous machinery technology, offering solutions to stabilize complex systems and maintain high performance in challenging, real-world environments.

### Fully Automated Crane: Developing Sway-Free Crane Automation Technology

In 2022, DeepX, in collaboration with Tadano Ltd. (hereafter referred to as Tadano), developed and announced a crane automation technology that carries out a three-axis lifting operation, which uses rotation, boom movement, and winching simultaneously, while keeping the load sway to a minimum.

#### Crane operation and the difficulty of its control

A crane is a piece of construction machinery engaged in lifting operations at various sites across a wide range of industries, including but not limited to construction and civil engineering.

Cranes have operating axes such as rotation, undulation, and winches, and are widely used to transport heavy loads from one point to another. Crane operators must simultaneously operate multiple levers, such as rotation, vertical motion, and winch, while visually checking the position of the load.

In particular, since the load is suspended by a wire, it undergoes pendulum motion. The phenomenon of the load swinging (“load swing”) is extremely dangerous because the load is heavy. If a person comes into contact with a swinging load, it can lead to a serious accident. Also, because the wire is long, it takes a long time for the load swing to naturally subside once it starts. In most cases, there are people waiting at the destination of the load, who perform a task called “unhooking,” which involves removing the load from the crane’s hook.
Therefore, operating while suppressing load swing is essential from the perspectives of safety and productivity.

#### The disturbances that make crane operation more challenging than it appears

Furthermore, crane operation is affected by disturbances such as mechanical deflection and wind. Due to the heaviness of the load, a phenomenon occurs where the arm or rod section (known as the “boom”) supporting the wire and the frame supporting the boom bends. The degree of bending is not uniform and varies depending on the load and posture. Under certain conditions, the tip of the boom can bend more than a meter, with a load. Operators must consider the degree of bending, which changes from moment to moment during operation, while moving the position of the load to the desired location.

On top of that, the behavior of the load changes due to the effect of the wind, behaving differently than in windless conditions. At construction sites, the wind may or may not blow depending on the day, location, and height. Sometimes the wind blows in a certain direction, and sometimes it suddenly blows in a random direction. Operators need to be flexible in responding to unexpected sudden wind movements of the load, while grasping the overall trend of the effects of the wind.

To cope with these disturbances, skilled expertise is required. It is said that mastery can take three to five years, and in some cases, as long as ten years.

#### The challenge of the industry and the significance of operation support and autonomous driving functions

On the other hand, in Japan, the number of construction workers is decreasing due to the decrease in the working-age population caused by the declining birthrate and aging population. The decrease in skilled operators who can freely operate construction machinery is also a major challenge. The mastery of crane operation often requires more years than the operation of other construction machinery, making this challenge even more serious.

This initiative aims to reduce the burden of crane operation and improve safety through assistive and automation functions. Specifically, DeepX are conducting research and development with the aim of improving on-site safety by simplifying, facilitating, automating, and making mobile crane operations more autonomous using robotic systems that perform real-time information processing, including AI.

#### The Developed Crane Automation Technology

In this initiative, the engineers developed crane automation technology that carries out a three-axis operation, a lifting operation that simultaneously uses rotation, undulation, and winch, while keeping the load swing to a minimum.

This technology, after performing the hooking operation (the task of hooking the load onto the hook at the end of the wire) and the ground-cutting operation (the operation of lifting the load from the ground), allows users to specify the rotation angle, working radius, and lifting height that correspond to the target coordinates where you want to carry the load. By running the autonomous driving program, it enables the automatic transportation of the load from any point in space to the specified target coordinates, while keeping the load swing to a minimum. Currently, the developed automation software is rated as having operational performance equivalent to that of an intermediate operator.

## References

https://www.deepx.co.jp/ja/