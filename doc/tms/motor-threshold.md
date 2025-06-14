
```{eval-rst}
.. include:: ../links.inc
```
# Automatic motor threshold estimation

This page describes the necessary setup, software and steps to automatically and rapidly estimate the {term}`motor threshold` resting  of any individual at the NMOD facility at Campus Biotech.

## Setup

- Connect the TMS ( {ref}`tms/magstim-super-rapid-plus:Magstim Super Rapid² Plus¹` / {ref}`tms/magstim-bistim:Magstim BiStim²`) to the NMOD desktop computer using the vendor serial cable.
- Turn on the EMG desktop WIFI {ref}`emg/noraxon:Noraxon` receiver and start MR3 software to control the Neuraxon.
- In MR3, go to Hardware Setup, and in General check that there is a delay of 156/96ms, then activate one DTS sensor corresponding to your EMG device (serial number on it).
- Turn on the CED Power3 1401 and connect the relevant EMG to the first digital port “0”.
- Connect the TMS Trigger Out coaxial output to the “Trigger” port of the CED Power3 1401.

## Software

Start `Matlab 2017b` on the NMOD facility desktop computer.
Run the code `MTAT_fcbg_rest.m`, a modified version of the program written by Prof. Dr. F. Awiszus ([Email Friedemann](mailto:friedemann.awiszus@med.ovgu.de)) compatible with the hardware available inside the NMOD facility.
 

The Matlab program `MTAT_fcbg_rest.m` connects to the TMS and iteratively:
- adjusts the TMS amplitude to minimize the uncertainty on the RMT wait for the TMS air trigger pedal to deliver the TMS pulse
- records the EMG and accepts / repeats the measurement based on the EMG baseline level before the TMS pulse analyzes the EMG data and calculates the 95% confidence interval on the RMT
- Exits the loop if RMT is certain.
 

```{note}
This process converges rapidly towards the RMT (~40 sec). If necessary, the default threshold(200 uV) can be easily modified in the code `MTAT_fcbg_rest.m` Do not start Signal in order to avoid CED control issues between Matlab and Signal.
```

```{figure} ../_static/motor/Tuto_MTAT_1.png
:align: center
:width: 600

Example of Matlab-based EMG data recording.
```

Counting the number of positive MEP (ie above RMT) is extremely time consuming and requires user interaction to count and/or adjust the TMS amplitude.
By contrast, the `MTAT_fcbg_rest.m` program is fast and fully automatic. The experimenter only needs to press the TMS pedal every 3 seconds to send the adjusted TMS pulse.

```{figure} ../_static/motor/Tuto_MTAT_2-980x530.png
:align: center
:width: 600

**On the left**: last EMG acquired. In the middle: next TMS amplitude. **One the right**: Summary of all peak-to-peak MEP data vs. TMS amplitude
```


## Bibliography
```{bibliography}
:filter: False
:list: bullet
AWISZUS200313
Lieberman1982
Pentland1980
AhSen2017
```