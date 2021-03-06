# Brevitas Model Results

<table>
<tr>
  <td> <b> Name </b> </td> <td> <b> Input Layers </b> </td> <td> <b> Eval Log Results </b> </td> <td> <b> Top1 Accuracy </b> </td> <td> <b> Notes </b> </td>
</tr>
<tr>
<td>
  
CNV_1W1A
  
</td>
<td> 
Original model 
  
```python
CNV_OUT_CH_POOL = [(64, False), (64, True), (128, False), (128, True), (256, False), (256, False)]
INTERMEDIATE_FC_FEATURES = [(256, 512), (512, 512)]
LAST_FC_IN_FEATURES = 512
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```  
</td>
<td>

```html
2021-07-22 18:19:39,045 Test: [90/100]  Model Time 0.010 (0.017)        Loss Time 0.000 (0.000) Loss 0.0969 (0.1081)    Prec@1 83.000 (81.473) Prec@5 100.000 (98.473)
2021-07-22 18:19:39,057 Test: [91/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.0865 (0.1079)    Prec@1 83.000 (81.489) Prec@5 98.000 (98.467)
2021-07-22 18:19:39,069 Test: [92/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.0945 (0.1077)    Prec@1 85.000 (81.527) Prec@5 99.000 (98.473)
2021-07-22 18:19:39,081 Test: [93/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.1281 (0.1080)    Prec@1 77.000 (81.479) Prec@5 97.000 (98.457)
2021-07-22 18:19:39,094 Test: [94/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.1008 (0.1079)    Prec@1 83.000 (81.495) Prec@5 99.000 (98.463)
2021-07-22 18:19:39,106 Test: [95/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.0810 (0.1076)    Prec@1 85.000 (81.531) Prec@5 100.000 (98.479)
2021-07-22 18:19:39,118 Test: [96/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.0890 (0.1074)    Prec@1 82.000 (81.536) Prec@5 100.000 (98.495)
2021-07-22 18:19:39,131 Test: [97/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.1471 (0.1078)    Prec@1 75.000 (81.469) Prec@5 99.000 (98.500)
2021-07-22 18:19:39,143 Test: [98/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.1234 (0.1080)    Prec@1 77.000 (81.424) Prec@5 99.000 (98.505)
2021-07-22 18:19:39,155 Test: [99/100]  Model Time 0.010 (0.016)        Loss Time 0.000 (0.000) Loss 0.1152 (0.1081)    Prec@1 74.000 (81.350) Prec@5 99.000 (98.510)
```
</td>

<td>
81.53%
</td>
<td>
  
Slows down at around 150 epochs. Pretrained model records top1 acc. at 84.22%.
  
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td> 
  
```python
CNV_OUT_CH_POOL = [(32, False), (32, True), (64, False), (64, True), (128, False), (128, False)]
INTERMEDIATE_FC_FEATURES = [(128, 256), (256, 256)]
LAST_FC_IN_FEATURES = 256
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```  
</td>
<td>

```html
2021-07-22 00:27:05,005 Test: [90/100]  Model Time 0.012 (0.017)        Loss Time 0.000 (0.000) Loss 0.1402 (0.1509)    Prec@1 71.000 (72.967) Prec@5 98.000 (97.088)
2021-07-22 00:27:05,025 Test: [91/100]  Model Time 0.016 (0.017)        Loss Time 0.001 (0.000) Loss 0.0991 (0.1504)    Prec@1 85.000 (73.098) Prec@5 99.000 (97.109)
2021-07-22 00:27:05,044 Test: [92/100]  Model Time 0.015 (0.017)        Loss Time 0.001 (0.000) Loss 0.1386 (0.1502)    Prec@1 77.000 (73.140) Prec@5 95.000 (97.086)
2021-07-22 00:27:05,061 Test: [93/100]  Model Time 0.014 (0.017)        Loss Time 0.000 (0.000) Loss 0.1535 (0.1503)    Prec@1 74.000 (73.149) Prec@5 96.000 (97.074)
2021-07-22 00:27:05,077 Test: [94/100]  Model Time 0.013 (0.017)        Loss Time 0.000 (0.000) Loss 0.1580 (0.1503)    Prec@1 69.000 (73.105) Prec@5 98.000 (97.084)
2021-07-22 00:27:05,094 Test: [95/100]  Model Time 0.014 (0.017)        Loss Time 0.000 (0.000) Loss 0.1105 (0.1499)    Prec@1 82.000 (73.198) Prec@5 99.000 (97.104)
2021-07-22 00:27:05,107 Test: [96/100]  Model Time 0.011 (0.017)        Loss Time 0.000 (0.000) Loss 0.1197 (0.1496)    Prec@1 78.000 (73.247) Prec@5 100.000 (97.134)
2021-07-22 00:27:05,120 Test: [97/100]  Model Time 0.010 (0.017)        Loss Time 0.000 (0.000) Loss 0.1981 (0.1501)    Prec@1 63.000 (73.143) Prec@5 97.000 (97.133)
2021-07-22 00:27:05,140 Test: [98/100]  Model Time 0.016 (0.017)        Loss Time 0.001 (0.000) Loss 0.1566 (0.1502)    Prec@1 71.000 (73.121) Prec@5 97.000 (97.131)
2021-07-22 00:27:05,160 Test: [99/100]  Model Time 0.016 (0.017)        Loss Time 0.001 (0.000) Loss 0.1453 (0.1501)    Prec@1 75.000 (73.140) Prec@5 99.000 (97.150)
```
</td>

<td>
73.24%
</td>
<td>
  
Converges/slows down a lot at 300th epoch. May observe noticeable growth later.
```bash
BREVITAS_JIT=1 brevitas_bnn_pynq_train --network CNV_1W1A --resume /path/to/checkpoint.tar
```
  
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td> 
  
```python
CNV_OUT_CH_POOL = [(16, False), (16, True), (32, False), (32, True), (64, False), (64, False)]
INTERMEDIATE_FC_FEATURES = [(64, 128), (128, 128)]
LAST_FC_IN_FEATURES = 128
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```
  </td>
<td>

```html
2021-07-22 06:00:06,800 Test: [90/100]  Model Time 0.007 (0.011)        Loss Time 0.000 (0.000) Loss 0.2057 (0.2209)    Prec@1 63.000 (59.286) Prec@5 92.000 (92.725)
2021-07-22 06:00:06,810 Test: [91/100]  Model Time 0.008 (0.011)        Loss Time 0.000 (0.000) Loss 0.1930 (0.2206)    Prec@1 67.000 (59.370) Prec@5 96.000 (92.761)
2021-07-22 06:00:06,828 Test: [92/100]  Model Time 0.015 (0.011)        Loss Time 0.000 (0.000) Loss 0.1911 (0.2203)    Prec@1 63.000 (59.409) Prec@5 96.000 (92.796)
2021-07-22 06:00:06,845 Test: [93/100]  Model Time 0.013 (0.011)        Loss Time 0.000 (0.000) Loss 0.2571 (0.2207)    Prec@1 47.000 (59.277) Prec@5 93.000 (92.798)
2021-07-22 06:00:06,861 Test: [94/100]  Model Time 0.012 (0.011)        Loss Time 0.000 (0.000) Loss 0.2209 (0.2207)    Prec@1 61.000 (59.295) Prec@5 94.000 (92.811)
2021-07-22 06:00:06,875 Test: [95/100]  Model Time 0.012 (0.011)        Loss Time 0.000 (0.000) Loss 0.1707 (0.2202)    Prec@1 75.000 (59.458) Prec@5 93.000 (92.812)
2021-07-22 06:00:06,889 Test: [96/100]  Model Time 0.011 (0.011)        Loss Time 0.000 (0.000) Loss 0.1918 (0.2199)    Prec@1 61.000 (59.474) Prec@5 94.000 (92.825)
2021-07-22 06:00:06,910 Test: [97/100]  Model Time 0.017 (0.012)        Loss Time 0.001 (0.000) Loss 0.2516 (0.2202)    Prec@1 52.000 (59.398) Prec@5 90.000 (92.796)
2021-07-22 06:00:06,928 Test: [98/100]  Model Time 0.015 (0.012)        Loss Time 0.000 (0.000) Loss 0.2367 (0.2204)    Prec@1 60.000 (59.404) Prec@5 92.000 (92.788)
2021-07-22 06:00:06,950 Test: [99/100]  Model Time 0.017 (0.012)        Loss Time 0.001 (0.000) Loss 0.2377 (0.2205)    Prec@1 56.000 (59.370) Prec@5 93.000 (92.790)
```

</td>
<td>
59.47%
</td>
<td>
Slows down at 150th epoch (little growth to 300th epoch)  
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td> 
  
```python
CNV_OUT_CH_POOL = [(8, False), (8, True), (16, False), (16, True), (32, False), (32, False)]
INTERMEDIATE_FC_FEATURES = [(32, 64), (64, 64)]
LAST_FC_IN_FEATURES = 64
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```
  </td>
<td>

```html
2021-07-22 19:10:04,518 Test: [90/100]  Model Time 0.010 (0.014)        Loss Time 0.000 (0.000) Loss 0.2932 (0.2761)    Prec@1 41.000 (46.648) Prec@5 91.000 (89.462)
2021-07-22 19:10:04,531 Test: [91/100]  Model Time 0.010 (0.014)        Loss Time 0.000 (0.000) Loss 0.2778 (0.2761)    Prec@1 46.000 (46.641) Prec@5 90.000 (89.467)
2021-07-22 19:10:04,544 Test: [92/100]  Model Time 0.010 (0.014)        Loss Time 0.000 (0.000) Loss 0.2434 (0.2758)    Prec@1 55.000 (46.731) Prec@5 94.000 (89.516)
2021-07-22 19:10:04,556 Test: [93/100]  Model Time 0.010 (0.014)        Loss Time 0.000 (0.000) Loss 0.2753 (0.2758)    Prec@1 45.000 (46.713) Prec@5 87.000 (89.489)
2021-07-22 19:10:04,567 Test: [94/100]  Model Time 0.009 (0.014)        Loss Time 0.000 (0.000) Loss 0.2530 (0.2755)    Prec@1 53.000 (46.779) Prec@5 93.000 (89.526)
2021-07-22 19:10:04,579 Test: [95/100]  Model Time 0.009 (0.014)        Loss Time 0.000 (0.000) Loss 0.2720 (0.2755)    Prec@1 50.000 (46.812) Prec@5 86.000 (89.490)
2021-07-22 19:10:04,591 Test: [96/100]  Model Time 0.010 (0.014)        Loss Time 0.000 (0.000) Loss 0.2699 (0.2754)    Prec@1 46.000 (46.804) Prec@5 89.000 (89.485)
2021-07-22 19:10:04,611 Test: [97/100]  Model Time 0.016 (0.014)        Loss Time 0.001 (0.000) Loss 0.2912 (0.2756)    Prec@1 41.000 (46.745) Prec@5 88.000 (89.469)
2021-07-22 19:10:04,629 Test: [98/100]  Model Time 0.015 (0.014)        Loss Time 0.000 (0.000) Loss 0.2789 (0.2756)    Prec@1 47.000 (46.747) Prec@5 89.000 (89.465)
2021-07-22 19:10:04,646 Test: [99/100]  Model Time 0.013 (0.014)        Loss Time 0.000 (0.000) Loss 0.2627 (0.2755)    Prec@1 51.000 (46.790) Prec@5 87.000 (89.440)
```

</td>
<td>
46.81%
</td>
<td>
Trained for 160 epochs
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td>  
  
```python
CNV_OUT_CH_POOL = [(16, False), (16, True), (32, True), (32, True), (64, False), (64, False)]
INTERMEDIATE_FC_FEATURES = [(64, 128), (128, 64)]
LAST_FC_IN_FEATURES = 64
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 2
```  
</td>
<td>

```html
2021-07-23 00:15:12,665 Test: [90/100]  Model Time 0.008 (0.012)        Loss Time 0.000 (0.000) Loss 0.2663 (0.2779)    Prec@1 46.000 (46.297) Prec@5 91.000 (87.473)
2021-07-23 00:15:12,675 Test: [91/100]  Model Time 0.008 (0.012)        Loss Time 0.000 (0.000) Loss 0.2708 (0.2778)    Prec@1 48.000 (46.315) Prec@5 86.000 (87.457)
2021-07-23 00:15:12,685 Test: [92/100]  Model Time 0.008 (0.012)        Loss Time 0.000 (0.000) Loss 0.2514 (0.2775)    Prec@1 54.000 (46.398) Prec@5 87.000 (87.452)
2021-07-23 00:15:12,695 Test: [93/100]  Model Time 0.008 (0.012)        Loss Time 0.000 (0.000) Loss 0.2725 (0.2775)    Prec@1 45.000 (46.383) Prec@5 85.000 (87.426)
2021-07-23 00:15:12,704 Test: [94/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.2823 (0.2775)    Prec@1 43.000 (46.347) Prec@5 90.000 (87.453)
2021-07-23 00:15:12,713 Test: [95/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.2595 (0.2773)    Prec@1 56.000 (46.448) Prec@5 87.000 (87.448)
2021-07-23 00:15:12,722 Test: [96/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.2476 (0.2770)    Prec@1 54.000 (46.526) Prec@5 90.000 (87.474)
2021-07-23 00:15:12,732 Test: [97/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.3075 (0.2773)    Prec@1 36.000 (46.418) Prec@5 82.000 (87.418)
2021-07-23 00:15:12,741 Test: [98/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.2796 (0.2773)    Prec@1 48.000 (46.434) Prec@5 86.000 (87.404)
2021-07-23 00:15:12,750 Test: [99/100]  Model Time 0.007 (0.012)        Loss Time 0.000 (0.000) Loss 0.2793 (0.2774)    Prec@1 44.000 (46.410) Prec@5 87.000 (87.400)
```
</td>

<td>
46.52%
</td>
<td>
  
Trained for 160 epochs
  
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td>  
  
```python
CNV_OUT_CH_POOL = [(16, False), (16, True), (32, False), (32, True), (64, False), (64, False)]
INTERMEDIATE_FC_FEATURES = [(64, 256), (256, 256)]
LAST_FC_IN_FEATURES = 256
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```  
</td>
<td>

```html
2021-07-26 20:30:40,064 Test: [90/100]  Model Time 0.008 (0.015)        Loss Time 0.000 (0.000) Loss 0.2159 (0.2232)    Prec@1 56.000 (57.176) Prec@5 94.000 (93.066)
2021-07-26 20:30:40,074 Test: [91/100]  Model Time 0.008 (0.015)        Loss Time 0.000 (0.000) Loss 0.1955 (0.2229)    Prec@1 67.000 (57.283) Prec@5 91.000 (93.043)
2021-07-26 20:30:40,084 Test: [92/100]  Model Time 0.008 (0.015)        Loss Time 0.000 (0.000) Loss 0.2032 (0.2227)    Prec@1 60.000 (57.312) Prec@5 93.000 (93.043)
2021-07-26 20:30:40,094 Test: [93/100]  Model Time 0.008 (0.015)        Loss Time 0.000 (0.000) Loss 0.2322 (0.2228)    Prec@1 58.000 (57.319) Prec@5 90.000 (93.011)
2021-07-26 20:30:40,103 Test: [94/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.2489 (0.2231)    Prec@1 55.000 (57.295) Prec@5 86.000 (92.937)
2021-07-26 20:30:40,112 Test: [95/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.1929 (0.2228)    Prec@1 65.000 (57.375) Prec@5 94.000 (92.948)
2021-07-26 20:30:40,121 Test: [96/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.1968 (0.2225)    Prec@1 63.000 (57.433) Prec@5 88.000 (92.897)
2021-07-26 20:30:40,131 Test: [97/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.2654 (0.2230)    Prec@1 45.000 (57.306) Prec@5 87.000 (92.837)
2021-07-26 20:30:40,140 Test: [98/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.2335 (0.2231)    Prec@1 50.000 (57.232) Prec@5 98.000 (92.889)
2021-07-26 20:30:40,149 Test: [99/100]  Model Time 0.007 (0.015)        Loss Time 0.000 (0.000) Loss 0.2427 (0.2233)    Prec@1 56.000 (57.220) Prec@5 94.000 (92.900)
```
</td>

<td>
57.43%
</td>
<td>
  
Trained for 160 epochs
  
</td>
</tr>
<tr>
<td>
CNV_1W1A
</td>
<td>  
  
```python
CNV_OUT_CH_POOL = [(32, False), (32, True), (256, False), (256, True), (256, False), (256, False)]
INTERMEDIATE_FC_FEATURES = [(256, 512), (512, 512)]
LAST_FC_IN_FEATURES = 512
LAST_FC_PER_OUT_CH_SCALING = False
POOL_SIZE = 2
KERNEL_SIZE = 3
```  
</td>
<td>

```html
2021-07-27 00:25:07,447 Test: [90/100]  Model Time 0.008 (0.016)        Loss Time 0.000 (0.000) Loss 0.0960 (0.1075)    Prec@1 84.000 (81.363) Prec@5 99.000 (98.593)
2021-07-27 00:25:07,457 Test: [91/100]  Model Time 0.008 (0.016)        Loss Time 0.000 (0.000) Loss 0.0833 (0.1072)    Prec@1 85.000 (81.402) Prec@5 98.000 (98.587)
2021-07-27 00:25:07,467 Test: [92/100]  Model Time 0.008 (0.016)        Loss Time 0.000 (0.000) Loss 0.0783 (0.1069)    Prec@1 91.000 (81.505) Prec@5 100.000 (98.602)
2021-07-27 00:25:07,476 Test: [93/100]  Model Time 0.007 (0.016)        Loss Time 0.000 (0.000) Loss 0.1055 (0.1069)    Prec@1 79.000 (81.479) Prec@5 100.000 (98.617)
2021-07-27 00:25:07,486 Test: [94/100]  Model Time 0.007 (0.016)        Loss Time 0.000 (0.000) Loss 0.1169 (0.1070)    Prec@1 81.000 (81.474) Prec@5 96.000 (98.589)
2021-07-27 00:25:07,496 Test: [95/100]  Model Time 0.007 (0.016)        Loss Time 0.000 (0.000) Loss 0.0953 (0.1069)    Prec@1 83.000 (81.490) Prec@5 99.000 (98.594)
2021-07-27 00:25:07,505 Test: [96/100]  Model Time 0.007 (0.016)        Loss Time 0.000 (0.000) Loss 0.0940 (0.1067)    Prec@1 85.000 (81.526) Prec@5 99.000 (98.598)
2021-07-27 00:25:07,515 Test: [97/100]  Model Time 0.008 (0.016)        Loss Time 0.000 (0.000) Loss 0.1232 (0.1069)    Prec@1 76.000 (81.469) Prec@5 99.000 (98.602)
2021-07-27 00:25:07,534 Test: [98/100]  Model Time 0.015 (0.016)        Loss Time 0.001 (0.000) Loss 0.1279 (0.1071)    Prec@1 77.000 (81.424) Prec@5 96.000 (98.576)
2021-07-27 00:25:07,550 Test: [99/100]  Model Time 0.013 (0.015)        Loss Time 0.000 (0.000) Loss 0.1100 (0.1071)    Prec@1 82.000 (81.430) Prec@5 100.000 (98.590)
```
</td>

<td>
81.52%
</td>
<td>
  
Trained for ~160 epochs
  
</td>
</tr>
</table>
