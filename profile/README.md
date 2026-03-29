# Sentience Robotics

**Open Source Ecosystem for Humanoid Interaction and Control**

[![Discord](https://img.shields.io/discord/1272611839775084564?color=5865F2&label=Community&logo=discord&logoColor=white)](https://discord.gg/g4KNZ3eeBd)

If you want to exchange on our projects, share ideas, or get involved, please join us on our Discord server.

Sentience Robotics is an initiative developing a modular, full-stack framework for humanoid robots. Our goal is to move beyond simple teleoperation by creating a cohesive system where high level AI driven interaction meets robust, real time hardware control.

While our primary development and testing platform is [InMoov](https://inmoov.fr/), created by **Gael LANGEVIN**, our software architecture is designed to be adaptable to any humanoid platform.

## Project Structure

### [LUCY](https://github.com/Sentience-Robotics/lucy_control_panel) | The Platform Bridge
Lucy is the core interface layer. It serves as a ROS 2 based API that abstracts hardware complexities, allowing any robot to be controlled by external web clients or AI models.
* **Architecture:** Built with a **C++ core** for performance critical tasks, utilizing **Python launch scripts** for orchestration.
* **Hardware Control:** Integration with **ros2_control** to manage actuator states and command interfaces.
* **Modeling:** Uses **Xacro based URDFs** to define robot kinematics, enabling transitions between simulation and real hardware.
* **The Goal:** Connect any robotic platform to any high level controller by defining the actuator configuration and implementing a lightweight connection interface.

Alongside, we are also developing the Lucy Control Panel, a web interface that enables makers and researchers to monitor and control robotic platforms remotely.

---

### [HuRI](https://github.com/Sentience-Robotics/HuRI) | Human-Robot Interaction
HuRI is an AI centric framework focusing on how the machine speaks, remembers, and moves.
* **Speech-to-Speech (S2S):** A custom pipeline that handles real time voice recognition, passes it through a multi model architecture, and outputs low latency speech.
* **Memory Layers:** Implements a cognitive framework for short, medium, and long term memory, allowing the robot to maintain context over multiple sessions.
* **Kinematic Grounding:** HuRI computes spatial points and transmits them to the robot, ensuring that arm, head, and facial movements are procedurally generated to match the conversation.

---

### Thais | Hardware and Fabrication
The Thais team is responsible for the physical embodiment of the Sentience ecosystem.
* **InMoov Integration:** Maintaining and enhancing our local InMoov builds, iterating on the original designs for better durability and integration with modern servos.
* **Next-Gen Development:** We are currently prototyping a new hardware model designed to optimize the range of motion and weight distribution required for advanced HRI.

## Our Open Source Pledge
We believe that the future of robotics belongs to the community. Sentience Robotics is committed to keeping our software, documentation, and research open and accessible. By providing our tools under open source licenses, we aim to lower the barrier to entry for humanoid research and encourage a collaborative environment where developers can build upon our work without proprietary restrictions.

## Technical Stack
* **Middleware:** ROS 2 Humble
* **Control Framework:** ros2_control
* **Languages:** C++ for hardware interfaces and core API, Python for AI pipeline and launch system
* **Hardware Modeling:** URDF, Xacro, Mesh processing
* 
### Why InMoov?

We selected the **InMoov** platform, created by French sculptor and designer **Gael LANGEVIN**, as our primary testbed. Its **Creative Commons** licensing and established community make it an ideal foundation for rapid experimentation and collaborative development. By using a widely accessible open-source hardware standard, we ensure that our software remains verifiable and reproducible by researchers and makers worldwide.

<img src="https://github.com/user-attachments/assets/5527703e-4fa9-4ef3-88d6-c5726f98082a" width="50%">

## Documentation

Our projects are fully documented, you can access said documentation at [docs.sentience-robotics.fr]([https://docs.sentience-robotics.fr](https://docs.sentience-robotics.fr/s/pub/p/public-documentation-EExgMX2REV)).

## The teams

Our project is divided into 3 teams, each focusing on a specific aspect of the project:

### Lucy // Embedded Systems Team

- [Antoine ESMAN](https://github.com/Arcod7)
- [Axel CHYPRE](https://github.com/Cadavre-chan)
- [Charles MADJERI](https://github.com/charlesmadjeri)
- [Maël RABOT](https://github.com/Mael-RABOT)
- [Mathieu BOREL](https://github.com/m-brl)
- [Samuel BRUSCHET](https://github.com/sambrus)

### Huri // AI Team

- [Adrien AUDIARD](https://github.com/Popochounet)
- [Basile FOUQUET](https://github.com/b3ww)
- [Matthias VON RAKOWSKI](https://github.com/MatthiasvonRakowski)
- [Thomas POMMIER](https://github.com/thomas-pommier-epi)

### Thais // Hardware Team

- [Doriane BALLU](https://www.linkedin.com/in/doriane-ballu-9b787324a/)
- [Nathan BREANT]()

## Licences

All our project are licensed under the [GPL-3.0 License](https://www.gnu.org/licenses/gpl-3.0.fr.html) (GNU General Public License v3.0) if not otherwise specified.

Parts of our projects that are derived from InMoov files (including Blender models, CAD files, and STL files) are based on the original work by **Gael LANGEVIN**.

**Original Work:** InMoov by Gael Langevin  
**License:** [Creative Commons Attribution-NonCommercial (CC BY-NC)](https://creativecommons.org/licenses/by-nc/4.0/)  
**Source:** http://inmoov.fr/  
**Applies to:** Blender files, CAD files, STL files, and other 3D models derived from InMoov

## Contact

For any questions or inquiries, please contact us [here](mailto:contact@sentience-robotics.fr).
