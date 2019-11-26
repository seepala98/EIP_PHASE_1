# Log for 20 Epochs #

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 18s 300us/step - loss: 0.3408 - acc: 0.9428 - val_loss: 0.0961 - val_acc: 0.9824
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 14s 235us/step - loss: 0.0959 - acc: 0.9833 - val_loss: 0.0535 - val_acc: 0.9884
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 13s 215us/step - loss: 0.0662 - acc: 0.9867 - val_loss: 0.0424 - val_acc: 0.9897
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 12s 202us/step - loss: 0.0515 - acc: 0.9885 - val_loss: 0.0331 - val_acc: 0.9911
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 13s 214us/step - loss: 0.0435 - acc: 0.9900 - val_loss: 0.0284 - val_acc: 0.9921
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 12s 208us/step - loss: 0.0388 - acc: 0.9910 - val_loss: 0.0250 - val_acc: 0.9935
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 12s 206us/step - loss: 0.0334 - acc: 0.9918 - val_loss: 0.0251 - val_acc: 0.9926
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 13s 210us/step - loss: 0.0311 - acc: 0.9924 - val_loss: 0.0265 - val_acc: 0.9928
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 14s 226us/step - loss: 0.0277 - acc: 0.9930 - val_loss: 0.0224 - val_acc: 0.9934
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 12s 207us/step - loss: 0.0264 - acc: 0.9933 - val_loss: 0.0244 - val_acc: 0.9939
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 13s 218us/step - loss: 0.0252 - acc: 0.9937 - val_loss: 0.0242 - val_acc: 0.9932
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 13s 220us/step - loss: 0.0229 - acc: 0.9941 - val_loss: 0.0202 - val_acc: 0.9943
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 13s 219us/step - loss: 0.0209 - acc: 0.9951 - val_loss: 0.0214 - val_acc: 0.9940
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 12s 206us/step - loss: 0.0193 - acc: 0.9953 - val_loss: 0.0218 - val_acc: 0.9939
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 13s 211us/step - loss: 0.0190 - acc: 0.9949 - val_loss: 0.0205 - val_acc: 0.9944
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 13s 218us/step - loss: 0.0190 - acc: 0.9946 - val_loss: 0.0238 - val_acc: 0.9933
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 12s 197us/step - loss: 0.0175 - acc: 0.9957 - val_loss: 0.0193 - val_acc: 0.9941
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 12s 201us/step - loss: 0.0163 - acc: 0.9960 - val_loss: 0.0197 - val_acc: 0.9940
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 13s 214us/step - loss: 0.0166 - acc: 0.9955 - val_loss: 0.0203 - val_acc: 0.9944
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 12s 207us/step - loss: 0.0141 - acc: 0.9966 - val_loss: 0.0197 - val_acc: 0.9942
<keras.callbacks.History at 0x7f74f95bf240>

## model.evaluate() on test data: ##
[0.019706157046975568, 0.9942]

## Strategy to achieve the result ##

1. add the BatchNormalization() after every convolution.
2. change the Dropout() value from 0.1 to 0.05 as reduce overfitting and to make sure before max pooling there is no Dropout() and also before flattening there is no dropout()
3. Remove last but one convolutional layer as its simply adding params to the network and produces not much value ,this will help in reducing the params under 15k.
