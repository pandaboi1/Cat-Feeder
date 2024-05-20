# Automatic Cat-Feeder
### By Edwin Serna
![Groot](Images/Groot.png)

### Project Description: Automated Cat Feeder Using Arduino Uno WiFi Rev2

#### Overview

This project was created to relieve anxiety from being away from home for extended periods, ensuring Groot is being fed on a strict schedule. By combining programming and DIY crafting skills, the project aims to create an automated cat feeder that can be easily replicated by anyone.

#### Objective

The objective of this project is to *design* and *create* an *automated cat feeder* that **dispenses food at predetermined times**, with the capability for **remote control** and **monitoring via Wi-Fi**.<br>
This will provide peace of mind for pet owners and ensure their pets are consistently fed, even when the owners are not present.

## Table of Contents
- [Setup](#setup)
    - [Components](#components)
        - [Arduino Uno WiFi Rev2 (x1)](#arduino-uno-wifi-rev2-x1-the-central-microcontroller-with-integrated-wi-fi-capabilities)
        - [Servo Motor (x1)](#servo-motor-x1-mechanism-for-dispensing-food)
        - [RTC (Real-Time Clock) Module (x1)](#rtc-real-time-clock-module-x1-to-maintain-accurate-feeding-schedules)
        - [Power Supply Cord (x1)](#power-supply-cord-x1-to-power-the-arduino-and-other-components)
        - [Food Container](#food-container-storage-for-the-cat-food)
        - [Dispensing Mechanism](#dispensing-mechanism-a-funnel-or-similar-setup-connected-to-the-servo-motor)
        - [Breadboard (x1) and Jumper Wires](#breadboard-x1-and-jumper-wires-for-prototyping-the-circuit) 
        - [Optional](#optional-push-buttons-or-lcd-display-for-setting-and-displaying-feeding-times)

- [Methodology](#methodology)
    1. [Hardware Setup](#1-hardware-setup)
    2. [Software Development](#2-software-development)
    3. [Dispensing Mechanism Construction](#dispensing-mechanism-a-funnel-or-similar-setup-connected-to-the-servo-motor)
    4. [Testing and Optimization](#4-testing-and-optimization)
- [Features](#features)
- [Benefits](#benefits)
- [Conclusion](#conclusion)

## Setup
### Components
#### **Arduino Uno WiFi Rev2 (x1)**: The central microcontroller with integrated Wi-Fi capabilities.
 - **($53.80)** [**Official Arduino Store** <br>ARDUINO UNO WiFi **REV2**](https://store-usa.arduino.cc/products/arduino-uno-wifi-rev2?queryID=undefined&selectedStore=us)
 - **($53.80)** [**Amazon** <br> Arduino UNO WiFi **REV2** [ABX00021]](https://www.amazon.com/dp/B07MK598QV?psc=1&ref=ppx_yo2ov_dt_b_product_details)


#### **Servo Motor (x1)**: Mechanism for dispensing food.
- **($6.50)** [**Official Arduino Store** <br>Grove - **Servo**](https://store-usa.arduino.cc/products/grove-servo?queryID=ccd898399d663fb795651f4c29768eaf&selectedStore=us) 
- **($6.99)** [**Amazon** <br>SG90 Micro **Servo Motor** for Arduino Raspberry Pi DIY (3 Pcs)](https://www.amazon.com/WWZMDiB-SG90-Control-Servos-Arduino/dp/B0BKPL2Y21/ref=sr_1_5?dib=eyJ2IjoiMSJ9.RcsIlcohLgaEgky6GIx3lU4pTO4z60pmQP3UXtrUBtGDlKOR8nKACI3Xkitj817yClHlmWgIC8EpkmqvPJ6DhRFyjgv1CPv4A0XknFAlpphMGeWOClfb7EtQv1x8qHKuWTCFhVRuiJT9cFCtX7uF4XMASFV516bYO-u1zmytXqUwhjhvXaT3Bzr61BG2lGxt_3seJZ_ci909a_qXKDYeukrwZD8AQycFnNR_AFdSTS0_oHwCtJg9q9j0WXssTyX6F4b0tmM9MibNrBSbtSydt46xvuOkQD0C1pAN8TxO5oM.OhQoEMcc7JY5EvPxbRuMEupASJqvHzH28GMrLvEPfJg&dib_tag=se&keywords=arduino%2Bservo%2Bmotor&qid=1716168221&sr=8-5&th=1) 

#### **RTC (Real-Time Clock) Module (x1)**: To maintain accurate feeding schedules.
- **($2.84)** [**Octopart** <br> Analog Devices **DS1307+**](https://octopart.com/ds1307%2B-maxim+integrated-998915)
- **($7.99)** [**Amazon**<br>AITRIP 3PCS DS3231 Real Time Clock Module **RTC Sensor** High Precision AT24C32 IIC Timer Alarm Clock for Arduino Raspberry Pi](https://www.amazon.com/dp/B09KPC8JZQ?ref=ppx_yo2ov_dt_b_product_details&th=1) 

#### **Power Supply Cord (x1)**: To power the Arduino and other components.
- **($9.99)** [**Amazon**<br> 9V 2A Power Supply Adapter AC DC **Cable** Cord for Arduino UNO MEGA, 5.5mm x 2.1mm & 2.5mm Plug, and More (6ft)](https://www.amazon.com/dp/B0852JLTL9/ref=sspa_dk_hqp_detail_aax_0?psc=1&sp_csd=d2lkZ2V0TmFtZT1zcF9ocXBfc2hhcmVk)

#### **Food Container**: Storage for the cat food.
- **($Variable)** Any malleable container you prefer

#### **Dispensing Mechanism**: A funnel or similar setup connected to the servo motor.
- **($Variable)** Any form of funneling you prefer

#### **Breadboard (x1) and Jumper Wires**: For prototyping the circuit.
- [**Official Arduino Store**](https://store-usa.arduino.cc)
    - **($4.00)** [**Breadboard** - 400 contacts](https://store-usa.arduino.cc/products/breadboard-400-contacts?pr_prod_strat=e5_desc&pr_rec_id=c34d03e87&pr_rec_pid=7198849073359&pr_ref_pid=7198886953167&pr_seq=uniform)
    - **($7.50)** [Breadboard **Jumper Wire** Pack (200mm&100mm)](https://store-usa.arduino.cc/products/breadboard-jumper-wire-pack-200mm-100mm?queryID=a0863cc40f9c6a18572f559986d4cb18&selectedStore=us)
- **($10.99)** [**Amazon** <br> Breadboard Jumper Wire Kit with **400-Point Breadboard**、**65pcs** Multiple Sizes M/M Bread Board **Jumper Wire**、**140 Pieces** 2-125 mm U-Shape Preformed **Jumper Wire** Kit](https://www.amazon.com/DaFuRui-Breadboard-400-Point-Multiple-Preformed/dp/B07KGQHJW8/ref=sr_1_3?crid=2822ZYIK6SPQT&dib=eyJ2IjoiMSJ9.pUTS4yU_X66oAAYeyCFRah8UFYh98OmGlkXzgI3MhITG3UN9TjR0k0Z9kHv-_Tv_j9gFkHbGHDyTwZNCC0S2SvRytbqeVBJ4wtDzCg7e_RYGT5yg63vYG3vTIgl_Qf2BZT3S9TZls4CH6th0fkbMDuxEaNTP1MxsiTEKlWdHefChBIXYgYFjJk8tIx5gv77OkCBPZxqqYSseE5ojAKb30TV9lD7wcn3mACsQH37GDqG-_m9G-G9WENda0aV3XAE6cIKRtvZNIsmrJ2ou_Vvwt2UYNCeD1DRmKT4OnCSNW3s.C5dwSmcVn8sveO9B7rDzNW-G-Q10df8T51J76lho2Rg&dib_tag=se&keywords=small+breadboard+and+wires&qid=1716171010&s=electronics&sprefix=small+breadboard+and+wires%2Celectronics%2C107&sr=1-3)

#### **Optional**: Push ***buttons*** or ***LCD display*** for setting and displaying feeding times.
- **Buttons**
    - **($8.00)** [**Official Ardunio Store** <br>Box 180 mixed **buttons**](https://store-usa.arduino.cc/products/box-180-mixed-buttons?queryID=8dce36eaded2030a3b344495131a81dc&selectedStore=us())
    - **($5.99)** [**Amazon** <br>QTEATAK 20 Pcs 6mm 2 Pin Momentary Tactile Tact **Push Button** Switch Through Hole Breadboard Friendly for Panel PCB](https://www.amazon.com/Momentary-Tactile-Through-Breadboard-Friendly/dp/B07WF76VHT/ref=sr_1_1_sspa?dib=eyJ2IjoiMSJ9.SoUcvBqaqaXOFdGNdo2igpBNtZW15Oh4VoCmvczxr7c0Hb9dAVRGE7TYFc3ffC6voSEQ7soadWEES-R8CxLRyITE3poqpLqUS_nFkofR2xVh9kQSlKh8ny4JMQCPdthn-zUzu7TDQVmoquJEYKu_C8Pq0n-Mv928EiXvZPCjbnqrbAR0GJvjZeAlicwNjgIDEH5GkqtzpwYWZ031Zcc7Xm7CAr4MwSkBSF2jGF6Hm8E.g1YDiKL2GvOm4KPO--0NAqUo-73Win4hpdrs7UmCrts&dib_tag=se&keywords=push+button+for+breadboard&qid=1716171420&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)
- **LCD display**
    - **($7.00)** [**Official Ardunio Store** <br>16x2 **LCD display** with I²C interface](https://store-usa.arduino.cc/products/16x2-lcd-display-with-i-c-interface?queryID=undefined&selectedStore=us)
    - **($8.99)** [**Amazon** <br>**2PCS** 1602 16x2 LCD Module Shield Yellow-Green Backlight with IIC I2C Driver Serial Interface and **LCD Module Display**](https://www.amazon.com/DORHEA-Yellow-Green-Backlight-Interface-Compatible/dp/B08TWPW7Q9/ref=sr_1_3?crid=3QYCRKRXX165D&dib=eyJ2IjoiMSJ9.oZ8JI31vw0Gno9ZyTbIBxQGe-0d613S2m4alqH5qE4QOeWwlGAQoN2Wv02M6XefFZ0YSFCddX54aE0ZUAggpzc4JPXWT9MfJLFsN9gztXDBg8TnjxbslLwxAXVEtn68_YmCSTePWJcc-nUDoW-qT5jzjmvu9D_YZ2lT7rMjKuUhy4PN01QkzinyJtiy1aczCH52O-acJuR4Z5HTc4DI807_7E1q4P0m75TZjCoFVi10.rHvL9IU9vGLdB3jE_6K4iUjBtIyekB62-pfnN0LUNWQ&dib_tag=se&keywords=16x2+LCD+display+with+I²C+interface&qid=1716172301&sprefix=16x2+lcd+display+with+i+c+interface%2Caps%2C190&sr=8-3)

## Methodology

#### 1. **Hardware Setup**:
   - Connect the servo motor to the Arduino Uno WiFi Rev2.
   - Integrate the RTC module to manage feeding times.
   - Establish power connections for all components.

#### 2. **Software Development**:
   - Install necessary libraries for the RTC and servo motor.
   - Develop and upload the code to control the feeding schedule and enable remote operation via Wi-Fi.
   - Implement a web interface for manual food dispensing.

#### 3. **Dispensing Mechanism Construction**:
   - Design and attach the servo-driven mechanism to the food container to dispense food at scheduled intervals.
   - Test and refine the dispensing system to ensure reliability.

#### 4. **Testing and Optimization**:
   - Simulate feeding times and adjust the system as needed.
   - Ensure the system functions correctly and the web interface operates smoothly for remote access.

## Features

- **Scheduled Feeding**: Automatically dispenses food at predefined times *using the RTC module*.
- **Remote Control**: Allows for manual food dispensing *via a web interface* accessible over Wi-Fi.
- **Secure Communication**: Utilizes the ATECC608A crypto authentication chip for secure data transmission.

## Benefits

- **Convenience**: Ensures pets are fed on time, reducing worry for pet owners who are away from home.
- **Scalability**: The project is designed to be easily replicable with commonly available components.
- **Learning Opportunity**: Combines programming and electronics skills, providing a valuable learning experience for students, hobbyists, and passionate creators willing to learn something new.

## Conclusion

This automated cat feeder project leverages Arduino Uno WiFi Rev2's capabilities to create a practical and replicable solution for pet care. <br>By following the outlined steps, **others** can ***build*** and ***customize*** their own automated feeders, enhancing pet care and owner peace of mind.