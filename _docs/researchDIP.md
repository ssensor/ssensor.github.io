---
layout: single
title: Perception 2D
permalink: /dlip/
sidebar:
  title: "Research"
  nav: "docs-research"
toc: true
toc_sticky: true
toc_label: "Research"
typora-copy-images-to: ..\assets\images
tags: dlip
entries_layout: grid
related: true
---

<br/>

<br/>

#  2D Object Detection

## YoffleNet: Light-Weight Object Detection for Embedded System
> 심이삭, 임주형, 장영완, 유지환, 오선택, & 김영근. (2021). 자율주행용 임베디드 플랫폼 탑재를 위한 YOLOv4 기반 객체탐지 경량화 모델 개발. 한국자동차공학회논문집, 29(10), 959-966.
>

The latest CNN-based object detection models are quite accurate, but they require a high-performance GPU to run in real-time. For an embedded system with limited memory space, they are still are heavy in terms of memory size and speed. This paper proposes YOffleNet, a new object detection model that is compressed at a high ratio while minimizing the accuracy loss for real-time and safe driving application on an autonomous system.

<img src="/docs/research/images/yofflenet.JPG" alt="yofflenet" style="zoom:75%;" />


<img src="../docs/research/images/demo.gif" alt="demo" style="zoom:75%;" />

[YOffleNet & Deep Sort for Tracking and Counting People](https://github.com/hkim1207/2021MIP)

<br/>

## A Lightweight CNN  for Detecting Defects in Substation Insulators with Drone EO/IR Camera

>SeonTaek Oh et al. "Development of a Compressed Deep Neural Network for Detecting Defected Electrical Substation Insulators using a Drone", Journal of Institute of Control, Robotics and Systems, vol.26 no.11, 2020

본 연구에서는 높은 정확도를 유지하면서도 경량화된 성능을 보유하는 YOffleNet 객체탐지 모델을 활용하여 열화상 이미지 기반 변전소 애자 및 코로나 검출을 진행하고자 한다.

<img src="../docs/research/images/corona-intro.png" alt="demo" style="zoom:75%;" />

<img src="../docs/research/images/corona1.png" alt="demo" style="zoom:75%;" />

### 


<br/>

<br/>



# Machine Vision for Smart Factory

## RGB-D 카메라 기반 고해상도 체적 측정 시스템 개발

사무실용 저가격/고해상도 체적 측정 시스템 개발을 위한 3D 카메라 기반 정형/비정형 물체 부피 측정 알고리즘 개발 (2019)

*  화물을 포함하는 최소 크기의 직육면체의 가로, 세로, 높이로 표현

* 해상도 및 정확도: 직육면체 ±5mm, 비정형 ±10mm 이내 만족

* 사각 50x50x50 ~ 600x600x600 mm$^3$,  원통 $\phi$  30 x 30 cm 

  

<img src="https://user-images.githubusercontent.com/38373000/167858513-3629986c-29e3-4658-9089-7b1038916d79.png" alt="image" style="zoom:80%;" />





## FPGA 기반 고속 임베디드 기어 검사 시스템 개발

> 오선택, 유지환, 김영근.(2019).고속 임베디드 기어 검사 시스템을 위한 불량 검출 알고리즘 FPGA 가속화 연구.제어로봇시스템학회 논문지,25(8),665-670.

기존 PC 기반 검출 시스템의 전력 소모를 줄이며 고속, 정밀한 불량 기어 검출 임베디드 시스템 구현을 위해 FPGA 기반 불량 기어 검출 영상처리 알고리즘을 제안한다. 병목현상이 나타나는 이진화 (Threshold), 모폴로지 (Morphology) 함수는 각각 6.2배, 49배의 가속화가 된 것을 확인하였으며, 기어 검수 알고리즘의 병목현상이 발생하는 Min Enclosing Circle의 경우, 함수 하드웨어 설계 및 데이터 개수 최소화 등의 방법을 통해 5.6배의 가속화를 하였다. 

<img src="https://user-images.githubusercontent.com/38373000/167859658-5b7ab527-f197-4202-8e42-f40ad4f7a9d4.png" alt="image" style="zoom:80%;" />

<img src="https://user-images.githubusercontent.com/38373000/167861700-1080a36f-5c2a-487b-a169-7abff69a7e62.png" alt="image" style="zoom:80%;" />

------

 <br/>




