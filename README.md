# 🌀 Maze Game

## 🔍 Overview

This project represents a computer system made in Quartus using FPGA, along with the program that
is executing on that system ( written in assembly ).

You can divide this computer system into 4 parts:

- CPU
- GPU
- RAM
- PS2 controller

## ⚙️ Prerequisites

- [Cyclon III FPGA](https://www.terasic.com.tw/cgi-bin/page/archive.pl?Language=English&No=118) 
with integrated SDRAM
- PS2 keyboard
- Monitor that has VGA output



## 🖥️ CPU

The CPU uses our small RISC architecture with 16 general-purpose registers. The instructions can be found in the Assembler folder.

## ⚡ GPU

The GPU is connected to the SDRAM, where it stores the color for each pixel on the screen and reads that memory when a refreshing cycle occurs. There are also functions to instruct the GPU to draw:
- pixel
- line
- rectangle

The GPU essentially stores different colors in its memory, which the user sees as a picture.

## 💾 RAM

RAM is the place where our instructions and data for our program are stored. When you start
the system, all data is loaded from the MIF files. You can see the content of the MIF file in the
Asembler folder.

## ⌨️ PS2 controller

The PS2 controller is used to receive data from the keyboard, store it in a register, and generate an interrupt request.

## 🚀 Program

The second part of the project is our program that is used to test our computer system.
That program contains maze games written in assembly for our architecture. It also contains
an assembly tool for translating it from symbolic machine language to MIF file, that will be
loaded in RAM.

What is used:

- VHDL
- C++
- Assembly
