---
layout: post
title: Pulse oximeters: wizardry or science?
---

We are surrounded by everyday objects that we have no idea how they work. One of them is pulse oximeters, used to monitor oxygen saturation and heart rate. herein, we will see its working principle and discover that it isn't witchcraft but science & technology.

### How it uses light to measure oxygen? 🤔

Pulse oximeters use simple optical technique but not so simple to write: _Photoplethysmography_ (PPG). This phenomenon was described in the 1930s by Alrick Hertzman. He chose the term _plethysmos_, derived from the Greek word _fullness_, based on his belief that his first observations were related to changes in blood volume. His theories were derived from the Beer-Lambert law, whose main premises were that the absorption of light is directly proportional to the path length, the concentration of substances and the absorption of light by each of these substances.

Through the PPG technique, optical properties of body tissue and blood can be characterized using a photodetector and red (660 nm) and infrared (940 nm) light sources. The intensity of the reflected light changes when the volume of the arterial vessel changes during the systolic phase, which is the ejection phase of blood during the cardiac cycle. This variation in light intensity is converted into an electrical signal by the oximeter. Pulsatile arterial blood absorbs and modulates the light emitted by the LEDs that passes through body tissue and forms the PPG signal. The AC component of this signal, represented by the light absorbed by pulsatile arterial blood, is the only variable term. While the DC component, represented by the light absorbed by non-pulsatile arterial blood, venous blood and tissues such as skin, nerves and bones, remains static.

The DC and AC components of the generated PPG signals are different for each LED. This is due to the distinct absorption characteristics of hemoglobin (Hb), oxyhemoglobin (HbO<sub>2</sub>) and other body tissue components for different wavelengths. From this difference, it is possible to calculate the oxygen saturation in the blood.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/ppg_diagram.png" width="600px" height="auto">

