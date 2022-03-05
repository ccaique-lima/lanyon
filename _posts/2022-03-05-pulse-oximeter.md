---
layout: post
title: "Pulse oximeters: wizardry or science?"
categories: []
tags: []
description:
---

We are surrounded by everyday objects that we have no idea how they work. One of them is pulse oximeter, used to monitor oxygen saturation and heart rate. Herein, we'll see its working principle and discover that it isn't witchcraft but science & technology.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/gollum_oximeter.png" width="200px" height="auto">

### How it uses light to measure oxygen? 🤔

Pulse oximeters use simple optical technique but not so simple to write: _Photoplethysmography_ (PPG). This phenomenon was described in the 1930s by Alrick Hertzman. He chose the term _plethysmos_, derived from the Greek word _fullness_, based on his belief that his first observations were related to changes in blood volume. His theories were derived from the Beer-Lambert law, whose main premises were that the absorption of light is directly proportional to the path length, the concentration of substances and the absorption of light by each of these substances.

Through the PPG technique, optical properties of body tissue and blood can be characterized using a photodetector and red (660 nm) and infrared (940 nm) light sources. The intensity of the reflected light changes when the volume of the arterial vessel changes during the systolic phase, which is the ejection phase of blood during the cardiac cycle. This variation in light intensity is converted into an electrical signal by the oximeter. Pulsatile arterial blood absorbs and modulates the light emitted by the LEDs that passes through body tissue and forms the PPG signal. The AC component of this signal, represented by the light absorbed by pulsatile arterial blood, is the only variable term. While the DC component, represented by the light absorbed by non-pulsatile arterial blood, venous blood and tissues such as skin, nerves and bones, remains static.

The DC and AC components of the generated PPG signals are different for each LED. This is due to the distinct absorption characteristics of hemoglobin (Hb), oxyhemoglobin (HbO<sub>2</sub>) and other body tissue components for different wavelengths. From this difference, it is possible to calculate the oxygen saturation in the blood.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/ppg_diagram.png" width="500px" height="auto">

<br>

### Is there a correct way to use it? Yea! 👍🏽

Many people don't know, but there is a correct way to use pulse oximeters to avoid measurement errors. The PPG signal is susceptible to external interference, mainly due to hand motion. So whenever you use a pulse oximeter, keep your hand at rest and avoid moving it.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/michelangelo_oximeter.png" width="500px" height="auto">

<br>

### Understanding the values

According to the WHO, oxygen saturation (SpO<sub>2</sub>) in healthy people of any age should be 95% or higher. If a person's SpO<sub>2</sub> is 94% or less, they should be evaluated quickly to identify and treat the cause. Levels below 90% are considered a clinical emergency and should be treated urgently!

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/spo2_level.png" width="500px" height="auto">

The heart rate (HR) is the number of times the heart beats per minute (bpm). The normal pulse for healthy adults ranges from 60 to 100 bpm. But athletes, who do a lot of cardiovascular conditioning, may have heart rates near 40 bpm. 😲

<br>

### References

ALIAN, A. A.; SHELLEY, K. H. Photoplethysmography. _Best Practice & Research Clinical Anaesthesiology_, v. 28, n. 4, p. 395–406, 4 2014.

Chacon, P.J., Pu, L., da Costa, T.H., Shin, Y.H., Ghomian,T., Shamkhalichenar, H., Wu, H.C., Irving, B.A., andChoi, J.W. (2019). A wearable pulse oximeter with wireless  communication and motion artifact tailoring for continuous use. _IEEE Transactions on Biomedical Engineering_, 66(6), 1505–1513.

Johns Hopkins Medicine. [Vital Signs (Body Temperature, Pulse Rate, Respiration Rate, Blood Pressure)](https://www.hopkinsmedicine.org/health/conditions-and-diseases/vital-signs-body-temperature-pulse-rate-respiration-rate-blood-pressure)

World Health Organization. [Pulse oximetry training manual](https://www.who.int/patientsafety/safesurgery/pulse_oximetry/who_ps_pulse_oxymetry_training_manual_en.pdf), 2011.





