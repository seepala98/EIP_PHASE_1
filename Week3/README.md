# Assignment 3 

## Final Validation Accuracy of base network :

Accuracy : 82.61 epoc: 46

## Model 
```
  model = Sequential()
  model.add(SeparableConv2D(48, (3, 3), padding='same', input_shape=(32, 32, 3),strides=(1,1))) #30 #3 
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(SeparableConv2D(96, (3, 3),strides=(1,1))) #28 #5
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(MaxPooling2D(pool_size=(2, 2))) #14  #6
  model.add(BatchNormalization())
  model.add(Dropout(0.05))
  model.add(SeparableConv2D(96, (3, 3),strides=(1,1))) #12  #10
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(SeparableConv2D(128, (3, 3),strides=(1,1))) #10  #14
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(MaxPooling2D(pool_size=(2, 2))) #5 #16
  model.add(BatchNormalization())
  model.add(Dropout(0.05))
  model.add(SeparableConv2D(96, (3, 3),strides=(1,1))) #3  #24
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(SeparableConv2D(64,(3, 3),strides=(1,1)))  #1  #32
  model.add(BatchNormalization())
  model.add(Activation('relu'))
  model.add(SeparableConv2D(num_classes, 3, padding='same', activation='softmax'))
  model.add(Flatten())

  model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
```

## model.summary():

```
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
separable_conv2d_1 (Separabl (None, 32, 32, 48)        219       
_________________________________________________________________
batch_normalization_1 (Batch (None, 32, 32, 48)        192       
_________________________________________________________________
activation_1 (Activation)    (None, 32, 32, 48)        0         
_________________________________________________________________
separable_conv2d_2 (Separabl (None, 30, 30, 96)        5136      
_________________________________________________________________
batch_normalization_2 (Batch (None, 30, 30, 96)        384       
_________________________________________________________________
activation_2 (Activation)    (None, 30, 30, 96)        0         
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 15, 15, 96)        0         
_________________________________________________________________
batch_normalization_3 (Batch (None, 15, 15, 96)        384       
_________________________________________________________________
dropout_1 (Dropout)          (None, 15, 15, 96)        0         
_________________________________________________________________
separable_conv2d_3 (Separabl (None, 13, 13, 96)        10176     
_________________________________________________________________
batch_normalization_4 (Batch (None, 13, 13, 96)        384       
_________________________________________________________________
activation_3 (Activation)    (None, 13, 13, 96)        0         
_________________________________________________________________
separable_conv2d_4 (Separabl (None, 11, 11, 128)       13280     
_________________________________________________________________
batch_normalization_5 (Batch (None, 11, 11, 128)       512       
_________________________________________________________________
activation_4 (Activation)    (None, 11, 11, 128)       0         
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 5, 5, 128)         0         
_________________________________________________________________
batch_normalization_6 (Batch (None, 5, 5, 128)         512       
_________________________________________________________________
dropout_2 (Dropout)          (None, 5, 5, 128)         0         
_________________________________________________________________
separable_conv2d_5 (Separabl (None, 3, 3, 96)          13536     
_________________________________________________________________
batch_normalization_7 (Batch (None, 3, 3, 96)          384       
_________________________________________________________________
activation_5 (Activation)    (None, 3, 3, 96)          0         
_________________________________________________________________
separable_conv2d_6 (Separabl (None, 1, 1, 64)          7072      
_________________________________________________________________
batch_normalization_8 (Batch (None, 1, 1, 64)          256       
_________________________________________________________________
activation_6 (Activation)    (None, 1, 1, 64)          0         
_________________________________________________________________
separable_conv2d_7 (Separabl (None, 1, 1, 10)          1226      
_________________________________________________________________
flatten_1 (Flatten)          (None, 10)                0         
=================================================================
Total params: 53,653
Trainable params: 52,149
Non-trainable params: 1,504
_________________________________________________________________
```

## Logs with first 50 epocs values :

```
Epoch 1/50
390/390 [==============================] - 41s 105ms/step - loss: 1.6302 - acc: 0.4310 - val_loss: 1.2361 - val_acc: 0.5527
Epoch 2/50
390/390 [==============================] - 35s 91ms/step - loss: 1.1566 - acc: 0.5858 - val_loss: 1.0236 - val_acc: 0.6318
Epoch 3/50
390/390 [==============================] - 36s 92ms/step - loss: 1.0223 - acc: 0.6354 - val_loss: 0.9641 - val_acc: 0.6519
Epoch 4/50
390/390 [==============================] - 36s 93ms/step - loss: 0.9401 - acc: 0.6689 - val_loss: 0.9368 - val_acc: 0.6703
Epoch 5/50
390/390 [==============================] - 36s 92ms/step - loss: 0.8776 - acc: 0.6882 - val_loss: 0.8394 - val_acc: 0.7032
Epoch 6/50
390/390 [==============================] - 36s 92ms/step - loss: 0.8332 - acc: 0.7064 - val_loss: 0.8227 - val_acc: 0.7136
Epoch 7/50
390/390 [==============================] - 36s 91ms/step - loss: 0.7972 - acc: 0.7190 - val_loss: 0.7759 - val_acc: 0.7266
Epoch 8/50
390/390 [==============================] - 36s 92ms/step - loss: 0.7646 - acc: 0.7313 - val_loss: 0.7655 - val_acc: 0.7328
Epoch 9/50
390/390 [==============================] - 36s 92ms/step - loss: 0.7461 - acc: 0.7376 - val_loss: 0.7992 - val_acc: 0.7250
Epoch 10/50
390/390 [==============================] - 36s 92ms/step - loss: 0.7222 - acc: 0.7452 - val_loss: 0.7417 - val_acc: 0.7460
Epoch 11/50
390/390 [==============================] - 35s 88ms/step - loss: 0.6989 - acc: 0.7547 - val_loss: 0.7175 - val_acc: 0.7547
Epoch 12/50
390/390 [==============================] - 34s 88ms/step - loss: 0.6867 - acc: 0.7595 - val_loss: 0.7063 - val_acc: 0.7566
Epoch 13/50
390/390 [==============================] - 34s 88ms/step - loss: 0.6715 - acc: 0.7640 - val_loss: 0.6758 - val_acc: 0.7649
Epoch 14/50
390/390 [==============================] - 35s 89ms/step - loss: 0.6605 - acc: 0.7706 - val_loss: 0.7648 - val_acc: 0.7398
Epoch 15/50
390/390 [==============================] - 34s 87ms/step - loss: 0.6403 - acc: 0.7755 - val_loss: 0.6820 - val_acc: 0.7661
Epoch 16/50
390/390 [==============================] - 34s 88ms/step - loss: 0.6274 - acc: 0.7808 - val_loss: 0.6858 - val_acc: 0.7588
Epoch 17/50
390/390 [==============================] - 35s 89ms/step - loss: 0.6218 - acc: 0.7832 - val_loss: 0.7181 - val_acc: 0.7563
Epoch 18/50
390/390 [==============================] - 35s 90ms/step - loss: 0.6148 - acc: 0.7823 - val_loss: 0.6234 - val_acc: 0.7837
Epoch 19/50
390/390 [==============================] - 36s 91ms/step - loss: 0.5996 - acc: 0.7899 - val_loss: 0.6790 - val_acc: 0.7686
Epoch 20/50
390/390 [==============================] - 36s 91ms/step - loss: 0.5967 - acc: 0.7910 - val_loss: 0.6896 - val_acc: 0.7687
Epoch 21/50
390/390 [==============================] - 35s 90ms/step - loss: 0.5854 - acc: 0.7942 - val_loss: 0.6355 - val_acc: 0.7801
Epoch 22/50
390/390 [==============================] - 35s 90ms/step - loss: 0.5756 - acc: 0.7958 - val_loss: 0.6419 - val_acc: 0.7823
Epoch 23/50
390/390 [==============================] - 36s 92ms/step - loss: 0.5695 - acc: 0.8010 - val_loss: 0.6631 - val_acc: 0.7762
Epoch 24/50
390/390 [==============================] - 35s 91ms/step - loss: 0.5679 - acc: 0.8005 - val_loss: 0.6034 - val_acc: 0.7927
Epoch 25/50
390/390 [==============================] - 36s 91ms/step - loss: 0.5564 - acc: 0.8057 - val_loss: 0.6185 - val_acc: 0.7869
Epoch 26/50
390/390 [==============================] - 36s 92ms/step - loss: 0.5526 - acc: 0.8042 - val_loss: 0.6643 - val_acc: 0.7811
Epoch 27/50
390/390 [==============================] - 36s 91ms/step - loss: 0.5441 - acc: 0.8092 - val_loss: 0.6203 - val_acc: 0.7841
Epoch 28/50
390/390 [==============================] - 36s 92ms/step - loss: 0.5395 - acc: 0.8095 - val_loss: 0.5727 - val_acc: 0.8023
Epoch 29/50
390/390 [==============================] - 36s 92ms/step - loss: 0.5344 - acc: 0.8135 - val_loss: 0.5599 - val_acc: 0.8083
Epoch 30/50
390/390 [==============================] - 35s 91ms/step - loss: 0.5275 - acc: 0.8139 - val_loss: 0.5695 - val_acc: 0.8051
Epoch 31/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5226 - acc: 0.8171 - val_loss: 0.5684 - val_acc: 0.8059
Epoch 32/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5205 - acc: 0.8176 - val_loss: 0.5863 - val_acc: 0.8008
Epoch 33/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5161 - acc: 0.8199 - val_loss: 0.6164 - val_acc: 0.7898
Epoch 34/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5140 - acc: 0.8218 - val_loss: 0.6005 - val_acc: 0.7952
Epoch 35/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5046 - acc: 0.8224 - val_loss: 0.5541 - val_acc: 0.8088
Epoch 36/50
390/390 [==============================] - 34s 88ms/step - loss: 0.5017 - acc: 0.8248 - val_loss: 0.5871 - val_acc: 0.8041
Epoch 37/50
390/390 [==============================] - 34s 87ms/step - loss: 0.4953 - acc: 0.8257 - val_loss: 0.5526 - val_acc: 0.8140
Epoch 38/50
390/390 [==============================] - 34s 87ms/step - loss: 0.4964 - acc: 0.8261 - val_loss: 0.5889 - val_acc: 0.8038
Epoch 39/50
390/390 [==============================] - 35s 90ms/step - loss: 0.4900 - acc: 0.8268 - val_loss: 0.5469 - val_acc: 0.8122
Epoch 40/50
390/390 [==============================] - 35s 90ms/step - loss: 0.4890 - acc: 0.8282 - val_loss: 0.5438 - val_acc: 0.8165
Epoch 41/50
390/390 [==============================] - 36s 92ms/step - loss: 0.4830 - acc: 0.8294 - val_loss: 0.5600 - val_acc: 0.8136
Epoch 42/50
390/390 [==============================] - 35s 90ms/step - loss: 0.4781 - acc: 0.8329 - val_loss: 0.5954 - val_acc: 0.7998
Epoch 43/50
390/390 [==============================] - 35s 90ms/step - loss: 0.4781 - acc: 0.8317 - val_loss: 0.5481 - val_acc: 0.8122
Epoch 44/50
390/390 [==============================] - 35s 89ms/step - loss: 0.4715 - acc: 0.8343 - val_loss: 0.5457 - val_acc: 0.8151
Epoch 45/50
390/390 [==============================] - 35s 89ms/step - loss: 0.4725 - acc: 0.8339 - val_loss: 0.5332 - val_acc: 0.8188
Epoch 46/50
390/390 [==============================] - 34s 88ms/step - loss: 0.4721 - acc: 0.8344 - val_loss: 0.5172 - val_acc: 0.8261
Epoch 47/50
390/390 [==============================] - 34s 88ms/step - loss: 0.4598 - acc: 0.8383 - val_loss: 0.5212 - val_acc: 0.8184
Epoch 48/50
390/390 [==============================] - 34s 88ms/step - loss: 0.4659 - acc: 0.8357 - val_loss: 0.5441 - val_acc: 0.8152
Epoch 49/50
390/390 [==============================] - 35s 90ms/step - loss: 0.4535 - acc: 0.8397 - val_loss: 0.5458 - val_acc: 0.8150
Epoch 50/50
390/390 [==============================] - 36s 91ms/step - loss: 0.4546 - acc: 0.8401 - val_loss: 0.5843 - val_acc: 0.8029
Model took 1761.04 seconds to train

Accuracy on test data is: 80.29
```
