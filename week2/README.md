## EIP Session 2 Assignment

**1) Logs for 20 Epochs**

Total params: 13,482

Train on 60000 samples, validate on 10000 samples

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 16s 270us/step - loss: 0.2110 - acc: 0.9332 - val_loss: 0.0665 - val_acc: 0.9779
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 12s 200us/step - loss: 0.0684 - acc: 0.9788 - val_loss: 0.0341 - val_acc: 0.9886
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 12s 197us/step - loss: 0.0515 - acc: 0.9841 - val_loss: 0.0385 - val_acc: 0.9877
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 12s 194us/step - loss: 0.0437 - acc: 0.9862 - val_loss: 0.0340 - val_acc: 0.9881
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 12s 196us/step - loss: 0.0385 - acc: 0.9874 - val_loss: 0.0268 - val_acc: 0.9910
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 12s 200us/step - loss: 0.0360 - acc: 0.9885 - val_loss: 0.0271 - val_acc: 0.9910
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 12s 196us/step - loss: 0.0330 - acc: 0.9897 - val_loss: 0.0286 - val_acc: 0.9908
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 12s 196us/step - loss: 0.0307 - acc: 0.9898 - val_loss: 0.0265 - val_acc: 0.9914
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 12s 200us/step - loss: 0.0295 - acc: 0.9905 - val_loss: 0.0202 - val_acc: 0.9939
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 12s 193us/step - loss: 0.0275 - acc: 0.9910 - val_loss: 0.0210 - val_acc: 0.9934
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 12s 195us/step - loss: 0.0250 - acc: 0.9920 - val_loss: 0.0230 - val_acc: 0.9929
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 12s 198us/step - loss: 0.0255 - acc: 0.9918 - val_loss: 0.0212 - val_acc: 0.9938
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 12s 195us/step - loss: 0.0238 - acc: 0.9920 - val_loss: 0.0224 - val_acc: 0.9937
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 11s 192us/step - loss: 0.0227 - acc: 0.9929 - val_loss: 0.0195 - val_acc: 0.9938
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 11s 185us/step - loss: 0.0214 - acc: 0.9932 - val_loss: 0.0225 - val_acc: 0.9924
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 11s 184us/step - loss: 0.0203 - acc: 0.9935 - val_loss: 0.0204 - val_acc: 0.9935
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 11s 184us/step - loss: 0.0202 - acc: 0.9934 - val_loss: 0.0175 - val_acc: 0.9946
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 11s 183us/step - loss: 0.0209 - acc: 0.9930 - val_loss: 0.0174 - val_acc: 0.9949
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 11s 179us/step - loss: 0.0194 - acc: 0.9936 - val_loss: 0.0195 - val_acc: 0.9936
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 11s 179us/step - loss: 0.0188 - acc: 0.9938 - val_loss: 0.0171 - val_acc: 0.9948

**2) Result of model.evaluate()**

[0.017060908846731036, 0.9948]

**3) Strategy to get this result.**

The code is taken and have been updated from the Eight version of MNIST. I have done the following changes in order to get to the said results:

1. Number of kernels from second and third layer has been reduced to reduce the number of paramters.
2. I have also tried to reduce the gap between the accuracy of training and test accuracy with the use of batch normalization.
3. I have removed the BatchNormalization and Dropout functions after the last layer as the last layer is sacrosanct. we should always avoid any activation or normalization at this last layer.
