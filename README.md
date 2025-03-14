# Medical-Image-Capturing

## Table of Contents
1. [Introduction](#introduction)
2. [Image Processing](#image-processing)
3. [FPGA](#fpga)
4. [Solution](#solution)
5. [Technology](#technology)
6. [Links](#links)

## Introduction
Image processing is used to extract useful information from images. This information can be used for various purposes, such as object recognition, space exploration, medical diagnosis, and quality control. 

GPUs and CPUs are general-purpose processors, so their parallelism is limited. They also have latency because they need to fetch instructions and data from memory, causing delays. ASICs, on the other hand, are not reprogrammable, so updates require a new chip implementation. To overcome these limitations, FPGAs are a better choice for image processing applications. They offer:

- Higher parallelism
- Lower latency
- Lower power consumption
- Easier programming

The goal of this project is to implement a simple image processing system on an FPGA.

## Image Processing
Image processing is used to extract meaningful information from images. Some common applications include:

- **Object Recognition**
- **Medical Imaging**
- **Quality Control**
- **Space Exploration**
- **Multimedia Processing**
- **Image Restoration**
- **Image Enhancement**
- **Noise Cancelling**
- **Scientific Imaging**

![Qc](https://github.com/user-attachments/assets/79b71ca6-a44a-40c4-807e-c59fdebff08c)

![mi](https://github.com/user-attachments/assets/f2a663cc-fac5-419f-9abb-010a5636f9f1)


### Common Image Processing Applications

- **Computer Vision**: Automatic interpretation of images, used in self-driving cars, facial recognition, and medical image analysis.
- **Medical Imaging**: Enhancing the quality of medical images (X-rays, MRI scans, ultrasound) for better diagnosis.
- **Quality Control**: Inspecting products for defects using automated scanning.
- **Multimedia**: Enhancing videos and images by noise reduction, sharpening, and color adjustments.

### Levels of Image Processing
1. **Low Level**: Input and output are both images (e.g., noise reduction, contrast enhancement).
2. **Mid Level**: Input is an image, and output is extracted attributes (e.g., edge detection, segmentation).
3. **High Level**: Computer vision, making sense of recognized objects using AI.

### Image Processing Techniques
- **Noise Removal**: Eliminates unwanted noise such as Gaussian or salt-and-pepper noise.
- **Sharpening**: Improves image clarity by increasing contrast between adjacent pixels.
- **Contrast Enhancement**: Adjusts contrast for better visibility.
- **Edge Detection**: Identifies edges in an image.
- **Object Segmentation**: Divides an image into separate objects.
- **Shape Analysis**: Extracts object shapes from an image.
- **Color Manipulation**: Modifies image colors.
- **Image Compression**: Reduces image size while maintaining quality.
- **Image Restoration**: Restores corrupted images.

### Benefits of Image Processing
- Enhances image quality by removing noise and improving contrast.
- Extracts valuable information like object locations and scene characteristics.
- Automates manual tasks such as classification and object detection.
- Powers new applications in virtual and augmented reality.

## FPGA (Field Programmable Gate Array)
FPGAs are integrated circuits designed to be configured after manufacturing. FPGA configurations are typically specified using hardware description languages (HDLs).

### FPGA Features
- Contains an array of programmable logic blocks.
- Includes reconfigurable interconnects for wiring logic blocks.
- Supports complex combinational functions and simple logic gates.
- Can include memory elements like flip-flops or memory blocks.
- Allows flexible reconfiguration for various logic functions.

### Advantages of FPGAs
- **Flexibility**: Can be reprogrammed for different logic functions.
- **Performance**: Operates at high clock speeds for intensive computations.
- **Power Efficiency**: Consumes less power, suitable for battery-powered applications.
- **Cost-Effective**: More affordable than ASICs in certain applications.

### Disadvantages of FPGAs
- **Complexity**: Requires expertise in HDL programming and design.
- **Higher Cost**: Can be more expensive than standard ICs.
- **Time to Market**: FPGA-based solutions take longer to develop than ASICs.

## Solution
To overcome the limitations of CPUs and GPUs in image processing (such as limited parallelism, latency, complex programming, and high energy consumption), we use an FPGA for computations. The image is converted into a matrix using Python and then sent to the programmed FPGA. The FPGA processes the matrix and returns the results to the computer.

### Implementation Steps
1. Convert an image into a matrix using Python.
2. Send the matrix to the FPGA.
3. Process the matrix using Verilog-based HDL programming.
4. Return the processed results to the computer.
5. Begin with low-level image processing (grayscale images) and extend to color images.

### Data Flow
![Data Flow](https://github.com/user-attachments/assets/b0f0dcda-0b43-49d1-8041-965a935a5ba2)

## Technology Stack
- **Verilog**
- **System Verilog**
- **OpenCV**
- **NumPy**
- **Python**
- **Xilinx Vivado or Altera Quartus**
# IMAGE CAPTURING AND ANALYSING SYSTEM USING FPGA


# IMAGE CAPTURING AND ANALYSING SYSTEM USING FPGA

**Group Members:**
- EKANAYAKEE.M.M.U.B. (E/17/083)
- WEERASINGHE W.A.C.J. (E/19/423)
- GROUP 23

---

## INTRODUCTION

Image Processing is a multidisciplinary field that involves the analyzing and manipulation of digital images using computer algorithms. Image processing is used in many fields like medicine, agriculture, archeology, motor traffic control, aerospace investigations, scientific researches, etc. Hardware devices like CPU (Central Processing Unit), GPU (Graphical Processing Unit), FPGA (Field Programmable Gate Array), and ASIC (Application Specific Integrated Circuit) are vastly used for Image Processing. Among them, FPGA is very popular in the industries since it comes with features like customizability, real-time processing, parallel processing, energy efficiency, etc.

In this project, we are applying two simple image processing algorithms: **Averaging Filter** and **Median Filter**.

---

## TECHNOLOGY STACK

### Hardware Components
![image](https://github.com/user-attachments/assets/74b83288-86f3-445d-947a-b41b0be58c7b)


### Software Tools and Languages

![image](https://github.com/user-attachments/assets/987cdfe7-739e-452e-b0b9-d97b0ae363a4)


### Reasons for Technology Selection

- **FPGA Board**: We used the Altera Terasic DE2-115 because it was the only FPGA board available in our faculty. It comes with a Cyclone IV FPGA module and meets our requirements, including:
  - 3,888 KB embedded memory
  - 4 general-purpose PLLs
  - 40 GPIO pins (3.3V)
  - 50 kHz oscillation clock

- **TTL Converter**: Used to convert USB data to UART serial data. Jumper wires are used to connect the TTL converter to the FPGA (RX and TX).

- **SystemVerilog**: Used because it supports packed arrays in RTL and classes for verification purposes, making it a good HDL choice.

- **Verilog**: Used to wrap SystemVerilog modules to avoid multidimensional torques.

- **Python**: Simple and easy for scripting, with support for libraries like OpenCV, Numpy, PySerial, and Math.

---

## PROCEDURE

1. **Design Initial Block Diagram**: The circuit includes a filter module, UART to AXIS receiver, and AXIS to UART transmitter modules. A Skid buffer is added to handle potential backpressure of data from the UART to AXIS transmitter module.

![image](https://github.com/user-attachments/assets/1f54c362-9178-4236-826f-497053f6b62a)

2. **Design Algorithms**:
   - **Averaging Filter**: Uses an addition tree method to add numbers in the filter kernel.
   - **Median Filter**: Uses a bitonic sort method to sort elements in the filter kernel. Both methods support parallel processing, which is crucial for image processing.

3. **Design State Machines**:
   - State Machine for Skid Buffer
   - State Machine for UART to AXIS Converter
   - State Machine for AXIS to UART Converter
![image](https://github.com/user-attachments/assets/74930cea-a330-4314-ab8c-01fa5302e8e0)

![image](https://github.com/user-attachments/assets/304e6d02-7299-4df5-937c-153a986ea697)

4. **Write RTL in SystemVerilog**: Write RTL for individual modules with testbenches and simulate them.

5. **Wrap Modules in Verilog**: Wrap all modules using Verilog and simulate them. Below are the waveform graphs obtained from the filters:

 ![image](https://github.com/user-attachments/assets/6f4be09d-b219-410e-aa11-c4ffeb3e42bf)
![image](https://github.com/user-attachments/assets/6b802d87-8168-4e6a-834e-7743b032ad59)


6. **Create FPGA Project**:
   - Open Quartus Prime Lite.
   - Create a new project using the project wizard.
   - Import RTLs and compile them.
   - Select the Cyclone IV E family and device EP4CE115F29C7N.
![image](https://github.com/user-attachments/assets/c176a91e-2d93-414f-98d2-07a90332949f)

7. **Generate PLL**:
   - Search for PLL (Phase Locked Loop) in the IP catalog.
   - Create a PLL with an input of 50 MHz and an output of 1000 MHz.
   - Generate the PLL Verilog file and import it into the `fpga_module.sv` module.

![image](https://github.com/user-attachments/assets/e018c4a6-b2b1-45d6-b324-07ba00691f89)


8. **Assign GPIO Pins**:
   - Assign GPIO pins to the RX and TX ports of the filter module using the "Pin Planner."
   - Upload the firmware to the FPGA board.

9. **Connect TTL Converter**:
   - Connect the TTL converter to the FPGA board using jumper wires.

![image](https://github.com/user-attachments/assets/f061d205-3825-4bab-80fa-00de0f8f0a6b)


10. **Design Python Algorithm**:
    - Design an algorithm to read image data, send it to the FPGA, receive the output, and convert it back to an image.
![image](https://github.com/user-attachments/assets/29f16277-0256-422e-8db1-5ad147b16a8b)


11. **Run Python Script**:
    - Connect the TTL converter to USB.
    - Power up the FPGA.
    - Run the Python program and observe the output image.

---

## RESULTS

### Input Image (with Salt and Pepper Noise)

![image](https://github.com/user-attachments/assets/75558281-9d05-49b7-8f5f-d05c026c5313)


### Output Images

- **Median Filter Output**:
![image](https://github.com/user-attachments/assets/d6cec3ab-9b39-4d01-b3cf-aba03f8739cd)


- **Averaging Filter Output**:
![image](https://github.com/user-attachments/assets/c4913f7d-c549-4c1b-9a0f-d81100a60c5d)


---

## OBSERVATIONS AND CALCULATIONS

We calculated the time taken to process a 430x320 px image (Figure 10):

| Parameter                              | Value               |
|----------------------------------------|---------------------|
| Size of a pixel                        | 8 bits              |
| Number of pixels transmitting per block| 7 x 7 = 49          |
| Number of bits transmitting per block  | 49 x 8 = 392 bits   |
| Number of bits receiving per block     | 392 bits            |
| Baud rate of transmission              | 115,200 bits/second |
| Time to transmit/receive 1 block       | 392 x 2 / 115,200 = 0.0068 seconds |
| Pixels per image block                 | 5 x 5 = 25 pixels   |
| Total number of pixels in the image    | 430 x 320 = 137,600 pixels |
| Number of image blocks                 | 137,600 / 25 = 5,504 blocks |
| **Total time to process the image**    | 5,504 x 0.0068 = 37.4272 seconds |

**Observed time for the whole process**: 44.23 seconds

---

## DISCUSSION

The observed time is higher than the calculated time due to:
- Delays in transmission.
- Delays in processing (errors in FPGA).
- Backpressure from the filter module.
- Delays in the Python code.

UART is not suitable for real-time processing due to its slow speed. Protocols like Ethernet or PCI should be used for real-time processing.

---

## FIGURES

1. Block Diagram
2. State Machine of Skid Buffer
3. State Machine of UART to AXIS Converter
4. State Machine of AXIS to UART Converter
5. Median Filter Waveform
6. Averaging Filter Waveform
7. PLL Flow Chart
8. Connection Diagram
9. Python Algorithm Flow
10. Input Image
11. Median Filter Output
12. Averaging Filter Output

---


