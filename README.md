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

**Markdown** _here_. (Blank lines needed before and after!)

</td>
</tr>
</table>
