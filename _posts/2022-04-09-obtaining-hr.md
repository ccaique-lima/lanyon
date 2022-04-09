---
layout: post
title: "How to obtain pulse rate from photoplethysmographic (PPG) signal?"
categories: []
tags: []
description:
---

Have you ever wondered how your smartwatch measures your pulse rate? With some basic knowledge of electronics and physiology we can understand how this is done.

In this post, we will learn how to get heart rate (HR) using photoplethysmographic (PPG) signal. Additional information on how PPG signals work can be found in my other post [Pulse oximeters: wizardry or science?](https://ccaique-lima.github.io/webpage/2022/03/05/pulse-oximeter/)

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/wearing_smartwatch.jpg" width="200px" height="auto">

There are different ways to get pulse rate. We can use derivatives or the Fourier transform of a PPG signal to estimate how many times the heart beats per minute. Herein, I will describe two methods for this: HR _PPG differentials_ and _HR spectral analysis_.

<br>

### HR PPG differentials method

In this method, our knowledge of Calculus can be applied, especially the use of derivatives. We will use the absolute derivative of PPG signal to identify pulse peaks and estimate HR, it determines the number of times the heart beats. These peaks are generated in the systolic phase, and the interval at which they occur determines the duration of a cardiac cycle. In the figure below, it is possible to observe that the x-markers in the absolute derivative of the PPG signal determine the beginning of the cardiac cycle.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/ppg_hr_diff.jpg" width="300px" height="auto">

The number of pulse peaks that occur in a 60-second period determines the HR in bpm. In the example illustrated above, the HR can be obtained as follows:

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/hr_ppg_diff_equation.png" width="300px" height="auto">

where Tp<sub>i</sub> is the time at which the pulse peak occur of the i-th sample and n is the number of pulse peaks counted in a given window. In this example, HR measurements were estimated in a 6-second window, i.e., at each 6-second section a new measurement was computed from the samples corresponding to that section.



<br>

### Is there a correct way to use it? Yea! 👍🏽

Many people don't know, but there is a right way to use pulse oximeters to avoid measurement errors. The PPG signal is susceptible to external interference, mainly due to hand motion. So whenever you use a pulse oximeter, keep your hand at rest and avoid moving it.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/michelangelo_oximeter.png" width="500px" height="auto">

<br>

### Understanding the values

According to the WHO, oxygen saturation (SpO<sub>2</sub>) in healthy people of any age should be 95% or higher. If a person's SpO<sub>2</sub> is 94% or less, they should be evaluated quickly to identify and treat the cause. Levels below 90% are considered a clinical emergency and should be treated urgently!

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/spo2_level.png" width="500px" height="auto">

The heart rate (HR) is the number of times the heart beats per minute (bpm). The normal pulse for healthy adults ranges from 60 to 100 bpm. But athletes, who do a lot of cardiovascular conditioning, may have heart rates near 40 bpm. 😲

<br>

### References

ALIAN, A. A.; SHELLEY, K. H. Photoplethysmography. _Best Practice & Research Clinical Anaesthesiology_, v. 28, n. 4, p. 395–406, 4 2014.

Chacon, P.J., Pu, L., da Costa, T.H., Shin, Y.H., Ghomian,T., Shamkhalichenar, H., Wu, H.C., Irving, B.A., andChoi, J.W. A wearable pulse oximeter with wireless  communication and motion artifact tailoring for continuous use. _IEEE Transactions on Biomedical Engineering_, 66(6), 1505–1513, 2019.

Johns Hopkins Medicine. [Vital Signs (Body Temperature, Pulse Rate, Respiration Rate, Blood Pressure)](https://www.hopkinsmedicine.org/health/conditions-and-diseases/vital-signs-body-temperature-pulse-rate-respiration-rate-blood-pressure).

World Health Organization. [Pulse oximetry training manual](https://www.who.int/patientsafety/safesurgery/pulse_oximetry/who_ps_pulse_oxymetry_training_manual_en.pdf), 2011.




