---
layout: post
title: "How to obtain pulse rate from photoplethysmographic (PPG) signal?"
categories: []
tags: []
description:
---

Have you ever wondered how your smartwatch measures your pulse rate? With some basic knowledge of electronics and physiology we can understand how this is done.

In this post, we will learn how to get heart rate (HR) using photoplethysmographic (PPG) signal. Additional information on how PPG signals work can be found in my other post [Pulse oximeters: wizardry or science?](https://ccaique-lima.github.io/webpage/2022/03/05/pulse-oximeter/)

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/wearing_smartwatch.jpg" width="300px" height="auto">

There are different ways to get pulse rate. We can use derivatives or the [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform) of a PPG signal to estimate how many times the heart beats per minute. Herein, I will describe two methods for this: _HR PPG differentials_ and _HR spectral analysis_.

<br>

### HR PPG differentials method

In this method, our knowledge of Calculus can be applied, especially the use of derivatives. We will use the absolute derivative of PPG signal to identify pulse peaks and estimate HR, it determines the number of times the heart beats. These peaks are generated in the systolic phase, and the interval at which they occur determines the duration of a cardiac cycle. In the figure below, it is possible to observe that the x-markers in the absolute derivative of the PPG signal determine the beginning of the cardiac cycle.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/ppg_hr_diff.jpg" width="600px" height="auto">

The number of pulse peaks that occur in a 60-second period determines the HR in bpm. In the example illustrated above, the HR can be obtained as follows:

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/hr_ppg_diff_equation.png" width="300px" height="auto">

where Tp<sub>i</sub> is the time at which the pulse peak occur of the i-th sample and n is the number of pulse peaks counted in a given window. In this example, HR measurements were estimated in a 6-second window, i.e., at each 6-second section a new measurement was computed from the samples corresponding to that section.

<br>

### HR spectral analysis method

We can easily obtain the HR using the Fourier transform. For this, we calculate the DFT of the PPG signal as shown in the figure below. Normally, the spectrum of the PPG signal shows a high-amplitude peak located at the cardiac frequency. The x-marker on the graph is used to obtain cardiac frequency and then HR.

<img src="https://raw.githubusercontent.com/ccaique-lima/webpage/gh-pages/assets/ppg_hr_spec.jpg" width="500px" height="auto">



<br>

<!-- ### References

ALIAN, A. A.; SHELLEY, K. H. Photoplethysmography. _Best Practice & Research Clinical Anaesthesiology_, v. 28, n. 4, p. 395–406, 4 2014.

Chacon, P.J., Pu, L., da Costa, T.H., Shin, Y.H., Ghomian,T., Shamkhalichenar, H., Wu, H.C., Irving, B.A., andChoi, J.W. A wearable pulse oximeter with wireless  communication and motion artifact tailoring for continuous use. _IEEE Transactions on Biomedical Engineering_, 66(6), 1505–1513, 2019.

Johns Hopkins Medicine. [Vital Signs (Body Temperature, Pulse Rate, Respiration Rate, Blood Pressure)](https://www.hopkinsmedicine.org/health/conditions-and-diseases/vital-signs-body-temperature-pulse-rate-respiration-rate-blood-pressure).

World Health Organization. [Pulse oximetry training manual](https://www.who.int/patientsafety/safesurgery/pulse_oximetry/who_ps_pulse_oxymetry_training_manual_en.pdf), 2011. -->




