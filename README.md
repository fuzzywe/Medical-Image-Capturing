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

# Developing image capturing and analysing system using FPGA

---

<!-- 
This is a sample image, to show how to add images to your page. To learn more options, please refer [this](https://projects.ce.pdn.ac.lk/docs/faq/how-to-add-an-image/)

![Sample Image](./images/sample.png)
 -->


## Table of Contents
1. [Introduction](#introduction)
2. [Image processing](#Image-processing)
3. [FPGA](#FPGA)
4. [Solution](#Solution)
5. [Technology](#Technology)
6. [Links](#links)


## Introduction

The image processing is used to extract useful information from images. This information can be used for a variety of purposes, such as object recognition,space explotation, medical diagnosis, and quality control.Due to GPUs and CPUs are general purpose processers  parallelism is limited. GPUs and CPUs typically have latency  because they have to fetch instructions and data from memory, which can add a significant delay.ASIC is not reprogramble so new a update must done with new chip implementation.So to overcome that problems FPGAs are better choice for image processing applications. They offer better performance by highly parallelism, lower latency, lower power consumption, and easier programming.So the goal of the project is implement a simple image processing system in a FPGA.

## Image processing

Image processing used to extract useful information from images.This information can be used for a variety of purposes:
				
    				object recorgnizing
				Medical imaging
				Quality control
				Space exploration
  				Multimedia
				Image restoration
				Image enchance
				Noice cancelling
				Scientafic images

![Qc](./images/Qc.png) 
Quality control

![mi](./images/mi.jpg)
Medical imaging

## Some of the most common image processing applications include:

Computer vision: 
This is the field of artificial intelligence that deals with the automatic interpretation of images. Computer vision techniques are used in a wide variety of applications, such as self-driving cars, facial recognition, and medical image analysis.

Medical imaging: 
Image processing techniques are used to improve the quality of medical images, such as X-rays, MRI scans, and ultrasound images. This can help doctors to diagnose diseases more accurately.

Quality control: 
Image processing techniques are used to inspect products for defects. This is done by automatically scanning the images of products for any abnormalities.

Multimedia: 
Image processing techniques are used to enhance the quality of multimedia content, such as videos and images. This can be done by removing noise, sharpening the images, and adjusting the colors

## Image processing three different levels :

Low level: 
	Image processing(input and output is an image)
		
Mid level: 
	Image analysis(input is an image and the output is attributes extact from the image)

High level:
	Computer vission(making sense of recognized objects(AI))


## Image processing techniques:

Noise removal: This involves removing unwanted noise from an image, such as Gaussian noise or salt and pepper noise.
Sharpening: This involves improving the clarity of an image by increasing the contrast between adjacent pixels.
Contrast enhancement: This involves adjusting the contrast of an image to make it easier to see.
Edge detection: This involves identifying the edges in an image.
Object segmentation: This involves dividing an image into different objects.
Shape analysis: This involves extracting the shape of objects in an image.
Color manipulation: This involves changing the color of an image.
Image compression: This involves reducing the size of an image without losing too much information.
Image restoration: This involves restoring an image that has been corrupted by noise or other artifacts.

## Benefits of image processing:

It can be used to improve the quality of images, such as by removing noise or enhancing the contrast.
It can be used to extract useful information from images, such as the location of objects or the characteristics of a scene.
It can be used to automate tasks that are currently done manually, such as image classification or object detection.
It can be used to create new applications, such as virtual reality or augmented reality.

Image processing is a powerful tool that can be used to solve a wide variety of problems. As the field continues to grow, we can expect to see even more innovative applications of image processing in the future.

## FPGA-(Field Programmable Gate Array)

FPGA is an integrated circuit designed to be configured after manufacturing. The FPGA configuration is generally specified using a hardware description language (HDL).
FPGAs contain an array of programmable logic blocks, and a hierarchy of reconfigurable interconnects allowing blocks to be wired together. Logic blocks can be configured to perform complex combinational functions, or act as simple logic gates like AND and XOR. In most FPGAs, logic blocks also include memory elements, which may be simple flip-flops or more complete blocks of memory. Many FPGAs can be reprogrammed to implement different logic functions, allowing flexible reconfigurable computing as performed in computer software.

## Advantages of FPGAs over other types of integrated circuits :

Flexibility:
FPGAs can be reconfigured to implement different logic functions, making them ideal for applications that require a high degree of flexibility.

Performance:
FPGAs can be clocked at very high frequencies, making them ideal for applications that require high performance.
Power efficiency: FPGAs can be very power efficient, making them ideal for battery-powered applications.

Cost:
FPGAs can be relatively inexpensive, making them a cost-effective solution for many applications.

## Disadvantages:
Complexity: 
FPGAs can be complex to design and program, which can limit their adoption by some users.

Cost:
FPGAs can be more expensive than other types of integrated circuits, such as application-specific integrated circuits (ASICs).

Time to market:
FPGAs can take longer to bring to market than ASICs, which can be a disadvantage for some applications.

Overall, FPGAs are a powerful and versatile type of integrated circuit that can be used in a wide variety of applications. They offer a number of advantages over other types of integrated circuits, but they also have some disadvantages. The best choice of integrated circuit for a particular application will depend on the specific requirements of that application.

## Solution
To overcome the problems occur when using CPUs and GPUs to image processing as like as limited parallalism , latency, hard programming and energy consumption using a suitable FPGA to do calclulations for analysings and operations. Image converted to  matrix using python in computer and the matrix sent to the progeammed FPGA.FPGA Programme using HDL verilog.Then the matrix  manupiulation is done in the FPGA and the resault return to the computer.First goal to do law level image processing to gray images.Then improve for the colour images.

![Pro](./images/Pro.png)
Data Flow

## Technology
Verilog, 
system verilog,
OpenCV,
numpy,
python,
Xlinux Vivado or Altera Quartus

## Links

- [Project Repository](https://github.com/cepdnaclk/{{ page.repository-name }}){:target="_blank"}
- [Project Page](https://cepdnaclk.github.io/{{ page.repository-name}}){:target="_blank"}
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)


[//]: # (Please refer this to learn more about Markdown syntax)
[//]: # (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


## INTRODUCTION

Image Processing is a multidisciplinary field that involves the analyzing and manipulation of digital images using computer algorithms. Image processing is used in many fields like medicine, agriculture, archeology, motor traffic control, aerospace investigations, scientific researches, etc. Hardware devices like CPU (Central Processing Unit), GPU (Graphical Processing Unit), FPGA (Field Programmable Gate Array), and ASIC (Application Specific Integrated Circuit) are vastly used for Image Processing. Among them, FPGA is very popular in the industries since it comes with features like customizability, real-time processing, parallel processing, energy efficiency, etc.

In this project, we are applying two simple image processing algorithms: **Averaging Filter** and **Median Filter**.

---

## TECHNOLOGY STACK

### Hardware Components
![image](https://github.com/user-attachments/assets/9c52f243-6961-400f-a319-1905b6590abb)

### Software Tools and Languages
![image](https://github.com/user-attachments/assets/c29b22e8-81b4-452f-968b-91fb7cfc942b)

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

![image](https://github.com/user-attachments/assets/abd6ae6c-de06-425e-be15-dde3ed9a8934)



2. **Design Algorithms**:
   - **Averaging Filter**: Uses an addition tree method to add numbers in the filter kernel.
   - **Median Filter**: Uses a bitonic sort method to sort elements in the filter kernel. Both methods support parallel processing, which is crucial for image processing.

3. **Design State Machines**:
   - State Machine for Skid Buffer
   - State Machine for UART to AXIS Converter
   - State Machine for AXIS to UART Converter
![image](https://github.com/user-attachments/assets/01be76ea-c9c0-47f9-93ac-e58dae4c5e07)


4. **Write RTL in SystemVerilog**: Write RTL for individual modules with testbenches and simulate them.   ![image](https://github.com/user-attachments/assets/18d6ffb6-dd89-4601-8096-83de32f1ddac)

State Machine of UART to AXIS Converter

![image](https://github.com/user-attachments/assets/f699d64b-03ce-4d79-89a8-66155a6a93d5)


State Machine of AXIS to UART Converter
 


5. **Wrap Modules in Verilog**: Wrap all modules using Verilog and simulate them. Below are the waveform graphs obtained from the filters:

  ![image](https://github.com/user-attachments/assets/78de00ad-0ad9-4e83-bc72-5e182360bf18)

![image](https://github.com/user-attachments/assets/76e78723-5c23-41a0-ae22-6a96d9099d55)

Wave form of the Median filter. Here img_data is the randomly generated input data and final_img_exp is the calculated output data which is expected. rx_data is the output data from filter and as seen in 2 figures, rx_data and final_img_exp are equal, showing the success of the implementation of the filter.

![image](https://github.com/user-attachments/assets/0e087ef6-513b-41f9-b052-0c72bbc65a32)



![image](https://github.com/user-attachments/assets/af13b5bd-5ddd-4d0f-8e9f-6022f223af2b)


Wave form of Averaging filter gives successful results
6. **Create FPGA Project**:
   - Open Quartus Prime Lite.
   - Create a new project using the project wizard.
   - Import RTLs and compile them.
   - Select the Cyclone IV E family and device EP4CE115F29C7N.

7. **Generate PLL**:
   - Search for PLL (Phase Locked Loop) in the IP catalog.
   - Create a PLL with an input of 50 MHz and an output of 1000 MHz.
   - Generate the PLL Verilog file and import it into the `fpga_module.sv` module.

![image](https://github.com/user-attachments/assets/82ae23cb-020f-4f54-ba0b-cf72528a2f01)

Flow Chart for Programing an FPGA

8. **Assign GPIO Pins**:
   - Assign GPIO pins to the RX and TX ports of the filter module using the "Pin Planner."
   - Upload the firmware to the FPGA board.

9. **Connect TTL Converter**:
   - Connect the TTL converter to the FPGA board using jumper wires.

![image](https://github.com/user-attachments/assets/a6d96522-eb14-4e98-ba4c-224b5ed46166)


10. **Design Python Algorithm**:
    - Design an algorithm to read image data, send it to the FPGA, receive the output, and convert it back to an image.


11. **Run Python Script**:
    - Connect the TTL converter to USB.
    - Power up the FPGA.
    - Run the Python program and observe the output image.
![image](https://github.com/user-attachments/assets/9629ddc8-0453-40bb-bcb0-7798c0307311)


---

## RESULTS

### Input Image (with Salt and Pepper Noise)
![image](https://github.com/user-attachments/assets/52d54c9f-0ff4-4635-b9f7-c1d582184c85)


### Output Images

- **Median Filter Output**:
 ![image](https://github.com/user-attachments/assets/97ac26f8-6ebf-4b20-9412-400e1e857f58)


- **Averaging Filter Output**:
 ![image](https://github.com/user-attachments/assets/8b1664c6-f9db-4842-8d0c-edc5b32c6823)


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

**Note**: Replace `FigureX.png` with the actual image file names or links to the images.
