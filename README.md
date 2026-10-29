# Hi, I'm an Electrical & Electronic Engineering Undergraduate 👋

🎓 **University of Peradeniya, Sri Lanka**

I am an Electrical and Electronic Engineering undergraduate with a strong interest in Telecommunications and Networking, Artificial Intelligence, Machine Learning, Computer Vision, Embedded Systems, and Electrical Power Engineering.

I enjoy exploring how engineering principles, programming, and intelligent technologies can be combined to solve practical problems. My academic and project work spans machine learning research, wireless communication systems, embedded hardware, digital electronics, and renewable energy.

---

## 🧑‍💻 Technical Skills

- **Programming Languages:** Python, C, AVR Assembly
- **Artificial Intelligence:** Machine Learning, Computer Vision, Object Detection, Image Segmentation, Model Evaluation
- **Telecommunications:** Wireless Communication, RSSI Analysis, Antenna Alignment, RF-Based Systems
- **Embedded Systems:** Microcontrollers, Hardware–Software Integration, Digital Logic
- **Engineering Software:** MATLAB, Multisim, Proteus, PSCAD, AutoCAD
- **Research Skills:** Dataset Preparation, Experimental Analysis, Performance Evaluation, Technical Documentation

---

# 🚀 Engineering Projects

## 1. Post-Disaster Damage Assessment Using Machine Learning and Semantic Communication

**Domain:** Artificial Intelligence | Computer Vision | Disaster Management

### Project Overview
This research project focuses on identifying disaster-related damage from ground-level images to support post-disaster assessment and response. The broader objective is to explore how machine learning and semantic communication can help extract and deliver meaningful disaster information efficiently.

### Problem Statement
Following disasters such as landslides and severe flooding, assessing ground-level damage can be challenging because of difficult terrain, damaged infrastructure, varying lighting conditions, and limited access to affected locations. Manual assessment can also be time-consuming.

This project investigates computer vision techniques for identifying visible damage and supporting a more efficient assessment workflow.

### Objectives
- Detect disaster-related objects in ground-level images.
- Segment affected areas to investigate their spatial extent.
- Evaluate image quality and its relevance to reliable analysis.
- Develop a mobile application workflow for image submission and assessment.
- Explore semantic communication as a way to transmit relevant information rather than relying exclusively on raw image transmission.

### Dataset and Preparation
The object detection dataset contains **1,349 annotated ground-level images** collected from disaster-affected locations in Sri Lanka. The images were annotated and verified for four object classes:

- Landslide
- Uprooted Tree
- Structures
- Debris

The object detection dataset was divided into 1,079 training images and 270 validation images. A separate segmentation dataset contained 678 polygon-annotated images, with classes including Exposed Area, Debris, and Road.

### Methodology and Implementation

**Object Detection**

Three models were evaluated using the annotated dataset:
- YOLO11n
- YOLOv8s
- RT-DETR-l

The models were compared using detection performance, precision, inference latency, and model complexity.

**Image Segmentation**

The segmentation experiments explored U-Net, DeepLabV3+, Mask R-CNN, and YOLO11s-seg to identify affected regions and investigate complex terrain boundaries.

**Image Quality Assessment and Mobile Application**

The project also included image quality assessment and mobile application development as parts of the broader workflow, with the aim of supporting image-based damage assessment.

**Semantic Communication**

Semantic communication is an important research direction of the project. The intended focus is on representing and transmitting task-relevant information efficiently. Its implementation and evaluation should be distinguished from the completed model experiments.

### Object Detection Results

The lightweight YOLO11n model achieved the following results in the current experimental setup:

- Precision: **91.3%**
- mAP@50: **88.4%**
- Inference latency: **2.2 ms**
- Model parameters: **2.58 million**

RT-DETR-l achieved a higher mAP@50 of 90.1% in the reported comparison, while YOLO11n offered a lightweight alternative suitable for further deployment investigation.

### Challenges and Future Work
Challenges include complex terrain boundaries, visual similarity between damaged and unaffected regions, image blur, lighting variation, and occlusion. Future work includes further robustness testing, edge-device deployment, evaluation under challenging environmental conditions, and development of the semantic communication component.

**Technologies:** Python, Jupyter Notebook, Ultralytics YOLO, Computer Vision, Machine Learning

---

## 2. BeamPilot — Smart Auto-Aligning Antenna System with Real-Time Sector Visualizer

**Domain:** Telecommunications | Wireless Networking | Embedded Systems

### Project Overview
BeamPilot is a project focused on developing a portable system to assist with directional antenna alignment for point-to-point Wi-Fi and LoRa communication links. The concept combines wireless signal measurements, antenna positioning, and a visual interface to help identify a suitable antenna direction.

### Problem Statement
Manual alignment of directional antennas can be time-consuming and may require repeated measurements to identify a direction that provides a stronger received signal. A measurement-assisted system could simplify this process and make antenna alignment more systematic.

### Objectives
- Measure received signal strength at different antenna directions.
- Investigate a 360-degree directional scanning workflow.
- Identify directions associated with stronger signal reception.
- Explore automated alignment based on measurement feedback.
- Visualize directional measurements using a real-time sector coverage interface.

### Proposed Methodology
The system concept combines antenna movement, wireless measurements, embedded control, and a visualization interface.

1. **Directional Scanning:** Collect signal measurements at defined antenna angles.
2. **Signal Measurement:** Record Received Signal Strength Indicator (RSSI) values.
3. **Data Processing:** Group measurements by physical scan angle and calculate representative values.
4. **Alignment:** Use the measured signal pattern to investigate the strongest direction.
5. **Visualization:** Display directional measurements in a polar or sector-based view.

### Experimental Analysis
An initial dataset containing 905 RSSI readings was analysed. The readings were regrouped into approximately 13 measurement sets corresponding to physical scan directions at 30-degree intervals. This approach avoids incorrectly treating every logged reading as a separate angle across the full 360-degree sweep.

The analysis investigated signal-strength variations, stronger reception directions, and weaker signal regions. The measured results can help guide subsequent hardware alignment and visualization work.

### Expected Outcome
The intended outcome is an integrated antenna alignment assistant that combines signal measurement, directional scanning, and visual feedback. Final performance depends on the completed hardware integration and further validation.

**Technologies and Concepts:** Wi-Fi, LoRa, ESP32, ESP-NOW, RSSI Analysis, Python-Based Visualization

---

## 3. ESP32 RF-Synchronized Sound-Based Distance Measurement

**Domain:** Embedded Systems | Signal Processing | Measurement Systems

### Project Overview
This project explores distance measurement using sound-based timing and radio-frequency synchronization. It combines microcontroller-based control with measurement processing to investigate how synchronized events can be used to estimate distance.

### Problem Statement
Timing-based distance measurement requires accurate identification of the relevant signal events. Timing errors, inconsistent triggering, and processing delays can affect the reliability of the calculated distance.

### Objectives
- Explore RF-based synchronization between measurement events.
- Investigate sound-based timing as a distance measurement method.
- Implement the measurement and calculation workflow using embedded hardware.
- Analyse the relationship between measured time and estimated distance.
- Evaluate measurement consistency and potential sources of error.

### Methodology
The general measurement principle is to determine the relevant sound propagation time and use it to estimate distance.

For a one-way sound propagation measurement:

Distance = Speed of sound × Propagation time

If the measurement uses a round-trip echo, the calculation must account for the sound travelling to the target and back:

Distance = (Speed of sound × Round-trip time) / 2

RF synchronization can help coordinate measurement events, but the exact calculation depends on the implemented hardware arrangement and timing method.

### Engineering Considerations
Important considerations include synchronization accuracy, timing resolution, sound propagation conditions, signal detection, and repeatability. These factors should be evaluated using the actual experimental setup.

**Technologies and Concepts:** ESP32, RF Synchronization, Sound-Based Timing, Embedded Programming, Distance Estimation

---

## 4. Rooftop Solar Photovoltaic System Design

**Domain:** Electrical Power Engineering | Renewable Energy

### Project Overview
This project focuses on the engineering design of a rooftop solar photovoltaic (PV) system. It involves applying electrical engineering principles to investigate solar energy generation and the relationship between energy demand, PV capacity, and system configuration.

### Problem Statement
A rooftop PV installation must be designed according to the available roof area, expected energy demand, solar resource, electrical constraints, and equipment characteristics. Appropriate sizing is important for estimating system performance and selecting suitable components.

### Objectives
- Investigate the energy requirements of the intended installation.
- Determine an appropriate PV system capacity based on the design inputs.
- Explore PV panel arrangement and rooftop space requirements.
- Study relevant electrical system components and configuration.
- Estimate expected energy generation using appropriate assumptions.

### Design Methodology
A typical engineering workflow includes:

1. **Energy Assessment:** Estimate energy consumption from the available load information.
2. **PV Capacity Estimation:** Relate the required energy production to expected solar conditions and system losses.
3. **Panel Arrangement:** Investigate module placement and available roof area.
4. **Electrical Configuration:** Consider the appropriate inverter, protection, cabling, and system arrangement.
5. **Performance Estimation:** Evaluate expected generation using the selected design assumptions.

The final design values depend on the actual load profile, site conditions, panel specifications, and design calculations.

### Engineering Considerations
Key considerations include solar irradiance, shading, panel orientation, conversion losses, electrical protection, and the relationship between generation and consumption.

**Domain Knowledge:** Photovoltaic Systems, Electrical Design, Renewable Energy, Energy Estimation

---

## 5. AVR Assembly-Based Smart Lock

**Domain:** Embedded Systems | Microcontrollers | Digital Electronics

### Project Overview
This project explores an electronic access-control system implemented using AVR assembly programming. It combines low-level microcontroller programming with control logic to investigate the operation of a smart locking mechanism.

### Problem Statement
An electronic locking system must interpret user input, evaluate access conditions, and control the locking mechanism according to defined rules. Implementing these operations at assembly level provides practical experience with microcontroller instructions, input handling, and hardware control.

### Objectives
- Develop low-level control logic using AVR Assembly.
- Process user input according to the implemented access rules.
- Investigate the relationship between program logic and hardware outputs.
- Practise register operations, branching, and conditional execution.
- Test the system's behaviour under relevant input conditions.

### Implementation Approach
The implementation can be documented through the following engineering components:

- **Input Processing:** Read the inputs supported by the actual circuit.
- **Decision Logic:** Evaluate the input against the programmed access conditions.
- **Output Control:** Operate the relevant output or locking mechanism.
- **Testing:** Verify correct behaviour for valid and invalid input cases.

The exact input method, locking hardware, and access-control features should be described according to the implemented circuit and source code.

### Learning Outcomes
The project provides practical experience in assembly-level programming, microcontroller architecture, digital control logic, and hardware–software interaction.

**Technologies and Concepts:** AVR Assembly, Microcontrollers, Digital Electronics, Embedded Control

---

## 6. Logic-Gate-Based Line-Following Robot

**Domain:** Digital Electronics | Robotics | Control Logic

### Project Overview
This project investigates a line-following robot controlled using digital logic gates. It applies Boolean logic and sensor inputs to determine the control signals required to guide a robot along a marked path.

### Problem Statement
A line-following robot must respond to changes in sensor readings as it moves along a path. The relationship between the sensor states and motor-control signals must be designed so that the robot can respond appropriately to different path conditions.

### Objectives
- Develop a logic-based control strategy for line following.
- Investigate how sensor inputs determine the robot's direction.
- Apply Boolean expressions and truth tables to movement decisions.
- Study the relationship between digital logic and motor control.
- Evaluate the behaviour of the control circuit under different sensor conditions.

### Methodology
A typical logic-based design process involves:

1. Identifying the sensor input conditions.
2. Constructing a truth table for the required robot responses.
3. Deriving Boolean expressions for the control outputs.
4. Implementing the expressions using appropriate logic gates.
5. Testing the resulting control behaviour with the robot hardware.

The exact logic equations and circuit configuration should match the actual design used in the project.

### Engineering Concepts
The project demonstrates the application of Boolean algebra, combinational logic, sensor interfacing, and basic robotic control.

**Technologies and Concepts:** Digital Logic, Logic Gates, Boolean Algebra, Sensors, Motor Control

---

# 📚 Areas of Technical Interest

- Telecommunications and Wireless Networking
- Artificial Intelligence and Machine Learning
- Computer Vision and Image Processing
- Embedded Systems and Microcontrollers
- Signal Processing and Measurement Systems
- Electrical Power Engineering and Renewable Energy

# 🤝 Connect With Me

I am interested in learning, collaborating on engineering projects, and exploring opportunities that combine telecommunications, intelligent systems, and practical engineering.

- **LinkedIn:** [https://www.linkedin.com/in/kajanilani-selvakumar-09baa2396/)
- 

---

*This portfolio summarises selected academic and engineering projects. Project descriptions, implementation details, and results should be interpreted according to the actual work completed and documented for each project.*
