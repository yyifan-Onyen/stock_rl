
```bash
cd code/Transformer/script
sh train_mae.sh
```

2）Long-term state inference module training:

```bash
cd code/Transformer/script
sh train_pred_long.sh
```

3) Short-term state inference  module training:

```bash
cd code/Transformer/script
sh train_pred_short.sh
```

4) Select the best model of three state inference modules from '*code/Transformer/checkpoints/*' according to their performance on validation set and add them to '*code/Transformer/pretrained/*'

**OR** directly use the model which have been pretrained in advance by us (dir:'*code/Transformer/pretrained/csi/* ')

#### 2nd stage：Policy Learning

1) train SAC model (three state inference module's path can be changed in *train_rl.py* file)

```bash
python train_rl.py
```

2) get prediction result on test set from '*code/results/df_print/*'

