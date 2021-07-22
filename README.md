# Brevitas-Model-Results
Training smaller models on the CIFAR dataset

<table>
<tr>
  <td> <b> Input Layers </b> </td> <td> <b> Results (Last 10 Batches of Last Epoch) </b> </td> <td> <b> Top1 Accuracy </b> </td> <td> <b> Notes </b> </td>
</tr>
<tr>
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
</table>
