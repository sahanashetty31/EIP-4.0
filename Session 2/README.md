*** Logs for 20 epochs ***
Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.01.
60000/60000 [==============================] - 10s 161us/step - loss: 0.2459 - acc: 0.9404 - val_loss: 0.0589 - val_acc: 0.9844
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0075815011.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0821 - acc: 0.9762 - val_loss: 0.0478 - val_acc: 0.9862
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0061050061.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0616 - acc: 0.9819 - val_loss: 0.0414 - val_acc: 0.9872
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.005109862.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0521 - acc: 0.9843 - val_loss: 0.0350 - val_acc: 0.9888
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0043936731.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0509 - acc: 0.9848 - val_loss: 0.0319 - val_acc: 0.9903
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0038535645.
60000/60000 [==============================] - 7s 110us/step - loss: 0.0447 - acc: 0.9865 - val_loss: 0.0383 - val_acc: 0.9884
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.003431709.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0417 - acc: 0.9879 - val_loss: 0.0256 - val_acc: 0.9922
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0030931024.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0389 - acc: 0.9881 - val_loss: 0.0278 - val_acc: 0.9910
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0028153153.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0366 - acc: 0.9885 - val_loss: 0.0260 - val_acc: 0.9926
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0025833118.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0349 - acc: 0.9897 - val_loss: 0.0291 - val_acc: 0.9918
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0023866348.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0342 - acc: 0.9902 - val_loss: 0.0265 - val_acc: 0.9914
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.0022177866.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0341 - acc: 0.9900 - val_loss: 0.0214 - val_acc: 0.9934
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.002071251.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0324 - acc: 0.9900 - val_loss: 0.0224 - val_acc: 0.9933
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0019428793.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0305 - acc: 0.9907 - val_loss: 0.0223 - val_acc: 0.9928
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0018294914.
60000/60000 [==============================] - 7s 113us/step - loss: 0.0295 - acc: 0.9913 - val_loss: 0.0230 - val_acc: 0.9935
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0017286085.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0281 - acc: 0.9915 - val_loss: 0.0231 - val_acc: 0.9934
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.00163827.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0276 - acc: 0.9916 - val_loss: 0.0241 - val_acc: 0.9929
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0015569049.
60000/60000 [==============================] - 7s 111us/step - loss: 0.0277 - acc: 0.9915 - val_loss: 0.0242 - val_acc: 0.9937
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0014832394.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0271 - acc: 0.9916 - val_loss: 0.0221 - val_acc: 0.9939
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.00141623.
60000/60000 [==============================] - 7s 112us/step - loss: 0.0264 - acc: 0.9916 - val_loss: 0.0228 - val_acc: 0.9936

<keras.callbacks.History at 0x7f345cda6160>


*** Result of model.evaluate (on test data) ***

[0.022809729901637182, 0.9936]

*** Strategy to achieve the result ***
1. Reducing the number of kernels.
2. Changing the learning rate scheduler value.
