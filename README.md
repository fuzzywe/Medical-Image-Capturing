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

