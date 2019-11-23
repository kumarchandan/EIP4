## EIP Session 2 Assignment

**1) Logs for 20 Epochs**
Total params: 13,492
Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 16s 266us/step - loss: 0.0240 - acc: 0.9924 - val_loss: 0.0338 - val_acc: 0.9903
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0183 - acc: 0.9940 - val_loss: 0.0241 - val_acc: 0.9926
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0151 - acc: 0.9950 - val_loss: 0.0205 - val_acc: 0.9940
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 7s 108us/step - loss: 0.0141 - acc: 0.9955 - val_loss: 0.0224 - val_acc: 0.9933
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0133 - acc: 0.9958 - val_loss: 0.0187 - val_acc: 0.9941
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0128 - acc: 0.9959 - val_loss: 0.0177 - val_acc: 0.9941
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 6s 106us/step - loss: 0.0107 - acc: 0.9963 - val_loss: 0.0200 - val_acc: 0.9945
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0115 - acc: 0.9960 - val_loss: 0.0189 - val_acc: 0.9940
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0108 - acc: 0.9964 - val_loss: 0.0210 - val_acc: 0.9936
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0098 - acc: 0.9966 - val_loss: 0.0187 - val_acc: 0.9949
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0091 - acc: 0.9968 - val_loss: 0.0192 - val_acc: 0.9944
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0096 - acc: 0.9965 - val_loss: 0.0190 - val_acc: 0.9946
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0094 - acc: 0.9971 - val_loss: 0.0191 - val_acc: 0.9949
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0078 - acc: 0.9973 - val_loss: 0.0184 - val_acc: 0.9949
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0072 - acc: 0.9974 - val_loss: 0.0186 - val_acc: 0.9949
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0084 - acc: 0.9970 - val_loss: 0.0192 - val_acc: 0.9946
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 6s 107us/step - loss: 0.0079 - acc: 0.9972 - val_loss: 0.0197 - val_acc: 0.9946
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0071 - acc: 0.9975 - val_loss: 0.0185 - val_acc: 0.9948
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0071 - acc: 0.9979 - val_loss: 0.0188 - val_acc: 0.9948
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 6s 108us/step - loss: 0.0080 - acc: 0.9973 - val_loss: 0.0186 - val_acc: 0.9945

**2) Result of model.evaluate()**

[0.01864307678944988, 0.9945]

**3) Strategy to get this result.**

The code is taken and have been updated from the Eight version of MNIST. I have done the following changes in order to get to the said results:

1. Number of kernels from second and third layer has been reduced to control the number of paramters.
2. I have also tried to reduce the gap between the accuracy of training and test accuracy.
3. I have removed the BatchNormalization and Dropout functions after the last layer as the last layer is sacrosanct. we should always avoid any activation or normalization at this last layer.
