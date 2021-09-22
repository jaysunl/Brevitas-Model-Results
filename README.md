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
  searcher:
    bracket_rungs: []
    divisor: 4
    max_concurrent_trials: 0
    max_length:
      epochs: 32
    max_rungs: 5
    max_trials: 500
    metric: validation_accuracy
    mode: standard
    name: adaptive_asha
    smaller_is_better: true
    source_checkpoint_uuid: null
    source_trial_id: null
    stop_once: false
  ```
Key:
- **Bold** values represent model values we are interested in (shrinking the model) with respect to the original Brevitas model.  
- Plain values represent larger model parameters.

| Hyperparameters | Original | Trial 1045 | Trial 957 | Trial 1746 |
| --- | --- | --- | --- | --- |
| `epochs` | 1000 | 32 | 32 | 32 |
| `validation_accuracy`| 0.842200 | 0.847400 | 0.845800 | 0.840700 | 
| `act_bit_width` | 1 | 2 | 4 | 1 |
| `cnv_out_ch_0` | 64 | 128 | 128 | 128 |
| `cnv_out_ch_1` | 64 | 256 | 64 | 512 |
| `cnv_out_ch_2` | 128 | 256 | 512 | 128 |
| `cnv_out_ch_3` | 128 | 512 | 512 | 256 |
| `cnv_out_ch_4` | 256 | 256 | 512 | 512 |
| `cnv_out_ch_5` | 256 | 512 | 512 | 512 |
| `cnv_pool_0` | `false` | `false` | `false` | `false` |
| `cnv_pool_1` | `true` | `true` | `true` | **`false`** |
| `cnv_pool_2` | `false` | `false` | `false` | `false` |
| `cnv_pool_3` | `true` | **`false`** | **`false`** | `true` |
| `cnv_pool_4` | `false` | `true` | `true` | `false` |
| `cnv_pool_5` | `false` | `true` | `false` | `false` |
| `int_fc_feat_1` | 512 | **16** | **32** | **256** |
| `int_fc_feat_2` | 512 | **128** | **64** | **32** |
| `kern_size` | 3 | 3 | **2** | **2** |
| `learning_rate` | 0.02 | 9.817997e-3 | 5.698063e-3 | 0.010601 |
| `pool_size` | 2 | 2 | 2 | 2 |
| `weight_bit_width` | 1 | 4 | 2 | 2 |

Hyperparameters used with varied strides:
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
  cnv_stride_0:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  cnv_stride_1:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  cnv_stride_2:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  cnv_stride_3:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  cnv_stride_4:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
  cnv_stride_5:
    type: categorical
    vals:
      - 1
      - 2
      - 3
      - 4
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
    minval: -5
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
  searcher:
    bracket_rungs: []
    divisor: 4
    max_concurrent_trials: 0
    max_length:
      epochs: 100
    max_rungs: 5
    max_trials: 500
    metric: validation_accuracy
    mode: standard
    name: adaptive_asha
    smaller_is_better: true
    source_checkpoint_uuid: null
    source_trial_id: null
    stop_once: false
  ```

With varied strides:
| Hyperparameters | Original | Trial 25878 | Trial 30314 | Trial 25815 |
| --- | --- | --- | --- | --- |
| `epochs` | 1000 | 100 | 100 | 100 |
| `validation_accuracy`| 0.842200 | 0.848300 | 0.778700 | 0.762100 | 
| `act_bit_width` | 1 | 4 | 4 | 4 |
| `cnv_out_ch_0` | 64 | 64 | 128 | 32 |
| `cnv_out_ch_1` | 64 | 32 | 128 | 32 |
| `cnv_out_ch_2` | 128 | 256 | 64 | 512 |
| `cnv_out_ch_3` | 128 | 128 | 64 | 128 |
| `cnv_out_ch_4` | 256 | 256 | 64 | 256 |
| `cnv_out_ch_5` | 256 | 512 | 256 | 32 |
| `cnv_pool_0` | `false` | `false` | `false` | `false` |
| `cnv_pool_1` | `true` | **`false`** | **`false`** | **`false`** |
| `cnv_pool_2` | `false` | **`false`** | **`false`** | **`false`** |
| `cnv_pool_3` | `true` | **`false`** | `true` | `true` |
| `cnv_pool_4` | `false` | `false` | `false` | `true` |
| `cnv_pool_5` | `false` | `false` | `false` | `false` |
| `cnv_stride_0` | 1 | 1 | 2 | 1 |
| `cnv_stride_1` | 1 | 1 | 2 | 1 |
| `cnv_stride_2` | 1 | 2 | 1 | 1 |
| `cnv_stride_3` | 1 | 1 | 1 | 1 |
| `cnv_stride_4` | 1 | 3 | 1 | 1 |
| `cnv_stride_5` | 1 | 4 | 2 | 3 |
| `int_fc_feat_1` | 512 | **256** | **16** | **256** |
| `int_fc_feat_2` | 512 | **32** | **64** | **32** |
| `kern_size` | 3 | 3 | **2** | 3 |
| `learning_rate` | 0.02 | 0.014109 | 8.059209e-3 | 8.508932e-3 |
| `pool_size` | 2 | 4 | 2 | 2 |
| `weight_bit_width` | 1 | 4 | 2 | 1 |
