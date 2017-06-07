---
layout: page
title: Portfolio
permalink: /portfolio/
---

### Personal Philosophy

Software is a craft and like fine furniture or art, it's something that requires pride and ownership. You have to be willing to change and grow daily, always looking for new ways to improve.

I consider myself a lifelong-learner. I learn by keeping up with the latest technology, tools and techniques. I listen to podcasts, chat with peers, and even traditional online professional development.

I "own" what I work on. I'm responsible for the quality, the performance and the adherence to specification. I'm responsible for my errors. The sooner they are discovered and reported, the sooner they can be fixed and the sooner the quality will be improved.

### Languages

- C++
- C#
- OpenCL
- Python
- Java
- LabVIEW
- Matlab

I am currently developing server software in C# to serve live video streams captured from HDMI devices for automated testing.

I am most experienced with C++, including modern C++ features included in C++14. I have developed applications handling image data and controlling PCI Express hardware. I have also developed parallel image processing algorithms either on the CPU or GPU using technologies such as CUDA and OpenCL. I have additional experience with languages such as Java, Python, LabVIEW and Matlab.

### Tools

<div class="row">
<div class="col-md-6">
- Visual Studio
- Git and Mercurial
- Static source analysis
- Unit testing
- Remote debugging
- Windows installer
</div>
<div class="col-md-6">
- Electronics testing
- Data acquisition
- Computer hardware
- PCI Express
- Serial
- Liquid crystal and eletro-optics
</div>
</div>

### Project: SLM Fluorescence Microscope

![SLM Microscope]({{ site.baseurl }}/images/optoscope.jpg){:width="50%"}

### Project: OverDrive Plus

![OverDrive Plus Response Time]({{ site.baseurl }}/images/overdrive.gif){:width="50%"}

OverDrive Plus is an implementation of an algorithm to increase the switching speed and uniformity of liquid crystal spatial light modulators. Several intermediate images are calculated from a target phase pattern and the current phase pattern. This calculation happens on the GPU using OpenCL. These images are then transfered to the spatial light modulator extremely fast. This gives the algorithm precise control over the pixel voltages over time, a key aspect to the algorithm.

### Project: Spatial Light Modulator Calibration

![Spatial Light Modulator System]({{ site.baseurl }}/images/slm_system.jpg){:width="50%"}

Liquid crystal phase shift versus voltage is non-linear and needs measurement and non-trivial calculation from the measurement data. I developed an automated calibration program using USB data acquisition and the device under test to measure this data and verify it's calibration. Ideally, the device should exhibit a linear phase shift from zero to two pi.

### Project: Polarization Hyperspectral Image Projector

I worked on a team of people to develop software and calibration of a projector used to test broadband imaging sensors for NASA. The projector used three liquid crystal on silicon spatial light modulators and a supercontinuum laser to create an image with precise spectrum, polarization and intensity control of each pixel. User control software was written in LabVIEW and C++ to integrate all hardware into an easy to use system.

### Contact me

[daneelshof@gmail.com](mailto:daneelshof@gmail.com)