---
layout: post
title: "Basic Fundamentals of Computer Vision"
date: 2024-08-22 10:00:00 +0900
author: Tri Thanh
categories: AI Engineer, Introducing
---

## Author: Tri Thanh


# Basic fundamentals of Computer Vision

Computer Vision (CV) is a major field within Artificial Intelligence (AI) that directly involves actions based on image data. Key domains within Computer Vision include Classification, Object Detection (OD), Optical Character Recognition (OCR), Image/Video Generation, among others. Computer Vision equips machines and automated systems with the ability to "see" like humans, allowing them to extract information from visible images with minimal human intervention during operation.

# Key domains

## Classification


The first domain in Computer Vision (CV) that has garnered attention since its inception and continues to be of interest today is Classification. Classification allows computers to categorize and identify objects in an image, determining which class the object belongs to among predefined classes that the model has been trained on, without human intervention.

-   **Popular Models**: AlexNet, VGG-16, ImageNet, ResNet50, etc.
-   **Strengths**: Simple model structure, low computational requirements, suitable for applications with limited hardware resources.
-   **Weaknesses**: Not suitable for object localization tasks or multi-object classification in a single image.
-   **Applications**: Classifying cats and dogs from a given image, determining whether a fruit is ripe or spoiled, etc.



## Object Detection


Object Detection is a significant area within Computer Vision that has garnered substantial interest in both research and practical applications. Unlike Classification, Object Detection addresses its limitations by enabling the identification of multiple objects within an image and simultaneously determining their locations. Additionally, Object Detection supports real-time operation and has numerous applications across various aspects of life.

-   **Popular Models**: Faster R-CNN, Mask R-CNN, YOLO, DETR, Vision Transformer, etc.
-   **Strengths**: Capable of recognizing multiple objects in a single image and pinpointing their exact locations. It can operate with streaming data in real-time.
-   **Weaknesses**: High computational demands, requiring significant hardware resources, making it unsuitable for edge devices with limited computational power.
-   **Applications**: Face recognition, intruder alert systems for residential areas, real-time waste detection on conveyor belts, etc.

Furthermore, Object Detection models are well-suited for Segmentation tasks (image partitioning) with minor structural modifications to the model.

## Optical Character Recognition


Optical Character Recognition (OCR) is an emerging field within Computer Vision that has garnered significant attention in recent applications. Similar to Object Detection, OCR involves one or more recognition models constructed through specific pipelines tailored to individual tasks and trained to accurately identify characters within images. OCR processes these recognized characters to reconstruct related information fields from the extracted text. This technology facilitates the automatic and rapid collection of information from images, effectively replacing manual data entry tasks.

-   **Popular Models**: Tesseract, EasyOCR, Surya, LLMs with Vision (Claude, Gemini, ChatGPT), etc.
-   **Strengths and Weaknesses**: Similar to Object Detection.
-   **Applications**: License plate recognition, character recognition from documents, etc.

## Image/Video Generation


Image/Video Generation is a rapidly growing field within Computer Vision that has captured significant attention recently. With advancements in hardware and the rise of Generative AI, Image/Video Generation has become increasingly prevalent and is continuously being refined through research in Generative AI and its applications in human life. Originating from classical generative models like GANs, the development of Diffusion models and Generative AI powered by Vision-Language Models (VLMs) promises even greater progress in the near future.

-   **Popular Models**: GAN, CycleGAN, Stable Diffusion, VLMs, etc.
-   **Strengths and Weaknesses**: Similar to Object Detection and OCR. For applications using Generative AI from third-party providers, additional costs for API and related extensions may apply.
-   **Applications**: Generating images from text descriptions, creating videos from discrete images, etc.

# Summary  
These key domains are commonly used in the Computer Vision tasks today. Additionally, there are numerous other methods and libraries that support these domains, which will be discussed in subsequent articles.