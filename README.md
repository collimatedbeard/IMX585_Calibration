# IMX585 Calibration Files
This repo contains calibration matrices and files for IMX585 sensor and libCamera.

This repository contains supporting files for yet unfinished episode of [Collimated Beard](https://youtu.be/CmViv5qjHJ4) dealing with color calibration of IMX585 sensor. 

Episode is not done yet, but that doesn't mean that you can't enjoy some better color on your Raspberry Pi now. (Yeah, you should totally subscribe)

## DNG
This is proper dual illuminant calibration which means that your DNG file should contain following information:
```
  "CalibrationIlluminant1": "StdA"
  "ColorMatrix1": [
    [  1.739500, -0.790900, -0.125400 ],
    [  0.038500,  0.829600,  0.100000 ],
    [  0.006900,  0.075100,  0.284800 ]]
  "ForwardMatrix1": [
    [  0.777100,  0.010000,  0.177200 ],
    [  0.355300,  0.446400,  0.198300 ],
    [  0.001700,  0.000200,  0.823300 ]]


  "CalibrationIlluminant2": "D55"
  "ColorMatrix2": [
    [  1.045000, -0.376900, -0.107400 ],
    [ -0.236100,  1.055800,  0.179000 ],
    [ -0.047900,  0.145700,  0.556400 ]]
  "ForwardMatrix2": [
    [  0.602000,  0.138500,  0.223900 ],
    [  0.217300,  0.712900,  0.069800 ],
    [  0.000300,  0.004200,  0.820600 ]]
```

## JSON Tunning File
In order to have auto white balance working properly, you will have to use imx585.json from this repository. CCMs have been recalculated for coefficients above, so whatever you are seeing on your screen should match the output of RAW converter.
