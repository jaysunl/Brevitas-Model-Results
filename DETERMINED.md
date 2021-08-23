# Determined Model Results
The following hyperparameters were used to train the CNN model using Determined AI's adaptive scan (ASHA) algorithm. The optimal results are shown below.
```yaml
hyperparameters:
  act_bit_width:
    type: categorical
    vals:
      - 1
      - 2
      - 4
  cnv_out_ch_0:
    type: categorical
    vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_out_ch_1:
    type: categorical
        vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_out_ch_2:
    type: categorical
    vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_out_ch_3:
    type: categorical
    vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_out_ch_4:
    type: categorical
    vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_out_ch_5:
    type: categorical
    vals:
      - 32
      - 64
      - 128
      - 256
      - 512
  cnv_pool_0:
    type: categorical
    vals:
      - true
      - false
  cnv_pool_1:
    type: categorical
    vals:
      - true
      - false
  cnv_pool_2:
    type: categorical
    vals:
      - true
      - false
  cnv_pool_3:
    type: categorical
    vals:
      - true
      - false
  cnv_pool_4:
    type: categorical
    vals:
      - true
      - false
  cnv_pool_5:
    type: categorical
    vals:
      - true
      - false
  global_batch_size:
    type: const
    val: 100
  int_fc_feat_1:
    type: categorical
    vals:
      - 16
      - 32
      - 64
      - 128
      - 256
      - 512
  int_fc_feat_2:
  type: categorical
    vals:
      - 16
      - 32
      - 64
      - 128
      - 256
      - 512
  kern_size:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  learning_rate:
  base: 10
    maxval: 0
    minval: -3
    type: log 
  learning_rate_decay:
    type: const
    val: 0
  pool_size:
    type: categorical
    vals:
      - 2
      - 4
  weight_bit_width:
    type: categorical
    vals:
      - 1     
      - 2     
      - 4
  ```
