# Assignment 4B : With GradCam 

### Best val_accracy: 0.8934 at (epoch:49)

```
Learning rate =  0.003
Model: "model_2"
__________________________________________________________________________________________________
Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_3 (InputLayer)            [(None, 32, 32, 3)]  0                                            
__________________________________________________________________________________________________
conv2d_42 (Conv2D)              (None, 32, 32, 16)   432         input_3[0][0]                    
__________________________________________________________________________________________________
batch_normalization_34 (BatchNo (None, 32, 32, 16)   64          conv2d_42[0][0]                  
__________________________________________________________________________________________________
activation_34 (Activation)      (None, 32, 32, 16)   0           batch_normalization_34[0][0]     
__________________________________________________________________________________________________
conv2d_43 (Conv2D)              (None, 32, 32, 32)   4608        activation_34[0][0]              
__________________________________________________________________________________________________
batch_normalization_35 (BatchNo (None, 32, 32, 32)   128         conv2d_43[0][0]                  
__________________________________________________________________________________________________
activation_35 (Activation)      (None, 32, 32, 32)   0           batch_normalization_35[0][0]     
__________________________________________________________________________________________________
conv2d_44 (Conv2D)              (None, 32, 32, 32)   9216        activation_35[0][0]              
__________________________________________________________________________________________________
conv2d_45 (Conv2D)              (None, 32, 32, 32)   512         activation_34[0][0]              
__________________________________________________________________________________________________
batch_normalization_36 (BatchNo (None, 32, 32, 32)   128         conv2d_44[0][0]                  
__________________________________________________________________________________________________
add_16 (Add)                    (None, 32, 32, 32)   0           conv2d_45[0][0]                  
                                                                 batch_normalization_36[0][0]     
__________________________________________________________________________________________________
activation_36 (Activation)      (None, 32, 32, 32)   0           add_16[0][0]                     
__________________________________________________________________________________________________
conv2d_46 (Conv2D)              (None, 32, 32, 32)   9216        activation_36[0][0]              
__________________________________________________________________________________________________
batch_normalization_37 (BatchNo (None, 32, 32, 32)   128         conv2d_46[0][0]                  
__________________________________________________________________________________________________
activation_37 (Activation)      (None, 32, 32, 32)   0           batch_normalization_37[0][0]     
__________________________________________________________________________________________________
conv2d_47 (Conv2D)              (None, 32, 32, 32)   9216        activation_37[0][0]              
__________________________________________________________________________________________________
batch_normalization_38 (BatchNo (None, 32, 32, 32)   128         conv2d_47[0][0]                  
__________________________________________________________________________________________________
add_17 (Add)                    (None, 32, 32, 32)   0           activation_36[0][0]              
                                                                 batch_normalization_38[0][0]     
__________________________________________________________________________________________________
activation_38 (Activation)      (None, 32, 32, 32)   0           add_17[0][0]                     
__________________________________________________________________________________________________
conv2d_48 (Conv2D)              (None, 32, 32, 64)   18432       activation_38[0][0]              
__________________________________________________________________________________________________
batch_normalization_39 (BatchNo (None, 32, 32, 64)   256         conv2d_48[0][0]                  
__________________________________________________________________________________________________
activation_39 (Activation)      (None, 32, 32, 64)   0           batch_normalization_39[0][0]     
__________________________________________________________________________________________________
conv2d_49 (Conv2D)              (None, 32, 32, 64)   36864       activation_39[0][0]              
__________________________________________________________________________________________________
conv2d_50 (Conv2D)              (None, 32, 32, 64)   2048        activation_38[0][0]              
__________________________________________________________________________________________________
batch_normalization_40 (BatchNo (None, 32, 32, 64)   256         conv2d_49[0][0]                  
__________________________________________________________________________________________________
add_18 (Add)                    (None, 32, 32, 64)   0           conv2d_50[0][0]                  
                                                                 batch_normalization_40[0][0]     
__________________________________________________________________________________________________
activation_40 (Activation)      (None, 32, 32, 64)   0           add_18[0][0]                     
__________________________________________________________________________________________________
conv2d_51 (Conv2D)              (None, 32, 32, 64)   36864       activation_40[0][0]              
__________________________________________________________________________________________________
batch_normalization_41 (BatchNo (None, 32, 32, 64)   256         conv2d_51[0][0]                  
__________________________________________________________________________________________________
activation_41 (Activation)      (None, 32, 32, 64)   0           batch_normalization_41[0][0]     
__________________________________________________________________________________________________
conv2d_52 (Conv2D)              (None, 32, 32, 64)   36864       activation_41[0][0]              
__________________________________________________________________________________________________
batch_normalization_42 (BatchNo (None, 32, 32, 64)   256         conv2d_52[0][0]                  
__________________________________________________________________________________________________
add_19 (Add)                    (None, 32, 32, 64)   0           activation_40[0][0]              
                                                                 batch_normalization_42[0][0]     
__________________________________________________________________________________________________
activation_42 (Activation)      (None, 32, 32, 64)   0           add_19[0][0]                     
__________________________________________________________________________________________________
conv2d_53 (Conv2D)              (None, 16, 16, 128)  73728       activation_42[0][0]              
__________________________________________________________________________________________________
batch_normalization_43 (BatchNo (None, 16, 16, 128)  512         conv2d_53[0][0]                  
__________________________________________________________________________________________________
activation_43 (Activation)      (None, 16, 16, 128)  0           batch_normalization_43[0][0]     
__________________________________________________________________________________________________
conv2d_54 (Conv2D)              (None, 16, 16, 128)  147456      activation_43[0][0]              
__________________________________________________________________________________________________
conv2d_55 (Conv2D)              (None, 16, 16, 128)  8192        activation_42[0][0]              
__________________________________________________________________________________________________
batch_normalization_44 (BatchNo (None, 16, 16, 128)  512         conv2d_54[0][0]                  
__________________________________________________________________________________________________
add_20 (Add)                    (None, 16, 16, 128)  0           conv2d_55[0][0]                  
                                                                 batch_normalization_44[0][0]     
__________________________________________________________________________________________________
activation_44 (Activation)      (None, 16, 16, 128)  0           add_20[0][0]                     
__________________________________________________________________________________________________
conv2d_56 (Conv2D)              (None, 16, 16, 128)  147456      activation_44[0][0]              
__________________________________________________________________________________________________
batch_normalization_45 (BatchNo (None, 16, 16, 128)  512         conv2d_56[0][0]                  
__________________________________________________________________________________________________
activation_45 (Activation)      (None, 16, 16, 128)  0           batch_normalization_45[0][0]     
__________________________________________________________________________________________________
conv2d_57 (Conv2D)              (None, 16, 16, 128)  147456      activation_45[0][0]              
__________________________________________________________________________________________________
batch_normalization_46 (BatchNo (None, 16, 16, 128)  512         conv2d_57[0][0]                  
__________________________________________________________________________________________________
add_21 (Add)                    (None, 16, 16, 128)  0           activation_44[0][0]              
                                                                 batch_normalization_46[0][0]     
__________________________________________________________________________________________________
activation_46 (Activation)      (None, 16, 16, 128)  0           add_21[0][0]                     
__________________________________________________________________________________________________
conv2d_58 (Conv2D)              (None, 8, 8, 256)    294912      activation_46[0][0]              
__________________________________________________________________________________________________
batch_normalization_47 (BatchNo (None, 8, 8, 256)    1024        conv2d_58[0][0]                  
__________________________________________________________________________________________________
activation_47 (Activation)      (None, 8, 8, 256)    0           batch_normalization_47[0][0]     
__________________________________________________________________________________________________
conv2d_59 (Conv2D)              (None, 8, 8, 256)    589824      activation_47[0][0]              
__________________________________________________________________________________________________
conv2d_60 (Conv2D)              (None, 8, 8, 256)    32768       activation_46[0][0]              
__________________________________________________________________________________________________
batch_normalization_48 (BatchNo (None, 8, 8, 256)    1024        conv2d_59[0][0]                  
__________________________________________________________________________________________________
add_22 (Add)                    (None, 8, 8, 256)    0           conv2d_60[0][0]                  
                                                                 batch_normalization_48[0][0]     
__________________________________________________________________________________________________
activation_48 (Activation)      (None, 8, 8, 256)    0           add_22[0][0]                     
__________________________________________________________________________________________________
conv2d_61 (Conv2D)              (None, 8, 8, 256)    589824      activation_48[0][0]              
__________________________________________________________________________________________________
batch_normalization_49 (BatchNo (None, 8, 8, 256)    1024        conv2d_61[0][0]                  
__________________________________________________________________________________________________
activation_49 (Activation)      (None, 8, 8, 256)    0           batch_normalization_49[0][0]     
__________________________________________________________________________________________________
conv2d_62 (Conv2D)              (None, 8, 8, 256)    589824      activation_49[0][0]              
__________________________________________________________________________________________________
batch_normalization_50 (BatchNo (None, 8, 8, 256)    1024        conv2d_62[0][0]                  
__________________________________________________________________________________________________
add_23 (Add)                    (None, 8, 8, 256)    0           activation_48[0][0]              
                                                                 batch_normalization_50[0][0]     
__________________________________________________________________________________________________
activation_50 (Activation)      (None, 8, 8, 256)    0           add_23[0][0]                     
__________________________________________________________________________________________________
global_average_pooling2d_2 (Glo (None, 256)          0           activation_50[0][0]              
__________________________________________________________________________________________________
dense_2 (Dense)                 (None, 10)           2560        global_average_pooling2d_2[0][0] 
==================================================================================================
Total params: 2,796,016
Trainable params: 2,792,144
Non-trainable params: 3,872
__________________________________________________________________________________________________
Using real-time data augmentation.
Learning rate =  0.003
Epoch 1/50
389/390 [============================>.] - ETA: 0s - loss: 2.0853 - acc: 0.3900Epoch 1/50
 77/390 [====>.........................] - ETA: 24s - loss: 2.0622 - acc: 0.3757WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 43s 109ms/step - loss: 2.0844 - acc: 0.3901 - val_loss: 2.0626 - val_acc: 0.3749
Learning rate =  0.003
Epoch 2/50
389/390 [============================>.] - ETA: 0s - loss: 1.5491 - acc: 0.5437Epoch 1/50
 79/390 [=====>........................] - ETA: 22s - loss: 1.5884 - acc: 0.5356WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 1.5486 - acc: 0.5440 - val_loss: 1.5884 - val_acc: 0.5356
Learning rate =  0.003
Epoch 3/50
389/390 [============================>.] - ETA: 0s - loss: 1.3866 - acc: 0.5962Epoch 1/50
 77/390 [====>.........................] - ETA: 23s - loss: 1.6358 - acc: 0.5304WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 1.3869 - acc: 0.5960 - val_loss: 1.6372 - val_acc: 0.5309
Learning rate =  0.003
Epoch 4/50
389/390 [============================>.] - ETA: 0s - loss: 1.3051 - acc: 0.6275Epoch 1/50
 77/390 [====>.........................] - ETA: 23s - loss: 1.8029 - acc: 0.4671WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 1.3049 - acc: 0.6276 - val_loss: 1.8079 - val_acc: 0.4659
Learning rate =  0.003
Epoch 5/50
389/390 [============================>.] - ETA: 0s - loss: 1.2342 - acc: 0.6608Epoch 1/50
 77/390 [====>.........................] - ETA: 23s - loss: 1.3856 - acc: 0.6139WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 1.2340 - acc: 0.6609 - val_loss: 1.3868 - val_acc: 0.6141
Learning rate =  0.0015
Epoch 6/50
389/390 [============================>.] - ETA: 0s - loss: 1.0423 - acc: 0.7261Epoch 1/50
 78/390 [=====>........................] - ETA: 23s - loss: 1.2926 - acc: 0.6378WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 1.0427 - acc: 0.7260 - val_loss: 1.2972 - val_acc: 0.6376
Learning rate =  0.0015
Epoch 7/50
389/390 [============================>.] - ETA: 0s - loss: 0.9872 - acc: 0.7417Epoch 1/50
 77/390 [====>.........................] - ETA: 24s - loss: 1.1399 - acc: 0.6888WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.9874 - acc: 0.7417 - val_loss: 1.1465 - val_acc: 0.6878
Learning rate =  0.0015
Epoch 8/50
389/390 [============================>.] - ETA: 0s - loss: 0.9451 - acc: 0.7538Epoch 1/50
 78/390 [=====>........................] - ETA: 24s - loss: 1.1562 - acc: 0.6805WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.9453 - acc: 0.7537 - val_loss: 1.1541 - val_acc: 0.6805
Learning rate =  0.0015
Epoch 9/50
388/390 [============================>.] - ETA: 0s - loss: 0.9108 - acc: 0.7678Epoch 1/50
 77/390 [====>.........................] - ETA: 24s - loss: 1.1465 - acc: 0.6985WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.9110 - acc: 0.7678 - val_loss: 1.1490 - val_acc: 0.6978
Learning rate =  0.0015
Epoch 10/50
389/390 [============================>.] - ETA: 0s - loss: 0.8908 - acc: 0.7760Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 1.2601 - acc: 0.6629WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.8909 - acc: 0.7761 - val_loss: 1.2584 - val_acc: 0.6625
Learning rate =  0.00075
Epoch 11/50
389/390 [============================>.] - ETA: 0s - loss: 0.7709 - acc: 0.8120Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.8724 - acc: 0.7708WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.7708 - acc: 0.8119 - val_loss: 0.8772 - val_acc: 0.7698
Learning rate =  0.00075
Epoch 12/50
389/390 [============================>.] - ETA: 0s - loss: 0.7446 - acc: 0.8178Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.8492 - acc: 0.7791WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 101ms/step - loss: 0.7444 - acc: 0.8178 - val_loss: 0.8491 - val_acc: 0.7791
Learning rate =  0.00075
Epoch 13/50
389/390 [============================>.] - ETA: 0s - loss: 0.7164 - acc: 0.8244Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.9660 - acc: 0.7568WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.7164 - acc: 0.8245 - val_loss: 0.9692 - val_acc: 0.7562
Learning rate =  0.00075
Epoch 14/50
389/390 [============================>.] - ETA: 0s - loss: 0.6969 - acc: 0.8274Epoch 1/50
 78/390 [=====>........................] - ETA: 25s - loss: 0.9010 - acc: 0.7667WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.6969 - acc: 0.8273 - val_loss: 0.9011 - val_acc: 0.7669
Learning rate =  0.00075
Epoch 15/50
389/390 [============================>.] - ETA: 0s - loss: 0.6741 - acc: 0.8354Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.7974 - acc: 0.7932WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 103ms/step - loss: 0.6743 - acc: 0.8354 - val_loss: 0.7973 - val_acc: 0.7922
Learning rate =  0.000375
Epoch 16/50
389/390 [============================>.] - ETA: 0s - loss: 0.6122 - acc: 0.8537Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.6935 - acc: 0.8272WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.6121 - acc: 0.8538 - val_loss: 0.6936 - val_acc: 0.8263
Learning rate =  0.000375
Epoch 17/50
389/390 [============================>.] - ETA: 0s - loss: 0.5838 - acc: 0.8645Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.6959 - acc: 0.8274WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.5839 - acc: 0.8644 - val_loss: 0.6968 - val_acc: 0.8271
Learning rate =  0.000375
Epoch 18/50
389/390 [============================>.] - ETA: 0s - loss: 0.5723 - acc: 0.8652Epoch 1/50
 79/390 [=====>........................] - ETA: 24s - loss: 0.6749 - acc: 0.8321WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.5724 - acc: 0.8651 - val_loss: 0.6749 - val_acc: 0.8321
Learning rate =  0.000375
Epoch 19/50
389/390 [============================>.] - ETA: 0s - loss: 0.5547 - acc: 0.8707Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.6608 - acc: 0.8371WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 101ms/step - loss: 0.5546 - acc: 0.8708 - val_loss: 0.6613 - val_acc: 0.8367
Learning rate =  0.000375
Epoch 20/50
389/390 [============================>.] - ETA: 0s - loss: 0.5460 - acc: 0.8729Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.6937 - acc: 0.8247WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.5458 - acc: 0.8730 - val_loss: 0.6931 - val_acc: 0.8240
Learning rate =  0.0001875
Epoch 21/50
389/390 [============================>.] - ETA: 0s - loss: 0.5061 - acc: 0.8866Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5764 - acc: 0.8621WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.5057 - acc: 0.8867 - val_loss: 0.5745 - val_acc: 0.8619
Learning rate =  0.0001875
Epoch 22/50
389/390 [============================>.] - ETA: 0s - loss: 0.4932 - acc: 0.8889Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5720 - acc: 0.8620WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4935 - acc: 0.8889 - val_loss: 0.5728 - val_acc: 0.8615
Learning rate =  0.0001875
Epoch 23/50
389/390 [============================>.] - ETA: 0s - loss: 0.4783 - acc: 0.8921Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5796 - acc: 0.8604WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.4784 - acc: 0.8921 - val_loss: 0.5806 - val_acc: 0.8597
Learning rate =  0.0001875
Epoch 24/50
389/390 [============================>.] - ETA: 0s - loss: 0.4694 - acc: 0.8966Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5746 - acc: 0.8615WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4692 - acc: 0.8967 - val_loss: 0.5739 - val_acc: 0.8609
Learning rate =  0.0001875
Epoch 25/50
389/390 [============================>.] - ETA: 0s - loss: 0.4629 - acc: 0.8972Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5695 - acc: 0.8599WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4630 - acc: 0.8972 - val_loss: 0.5701 - val_acc: 0.8594
Learning rate =  9.375e-05
Epoch 26/50
389/390 [============================>.] - ETA: 0s - loss: 0.4385 - acc: 0.9055Epoch 1/50
 77/390 [====>.........................] - ETA: 26s - loss: 0.5436 - acc: 0.8693WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 103ms/step - loss: 0.4385 - acc: 0.9055 - val_loss: 0.5431 - val_acc: 0.8692
Learning rate =  9.375e-05
Epoch 27/50
389/390 [============================>.] - ETA: 0s - loss: 0.4311 - acc: 0.9064Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5368 - acc: 0.8744WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.4309 - acc: 0.9064 - val_loss: 0.5396 - val_acc: 0.8740
Learning rate =  9.375e-05
Epoch 28/50
389/390 [============================>.] - ETA: 0s - loss: 0.4238 - acc: 0.9095Epoch 1/50
 78/390 [=====>........................] - ETA: 24s - loss: 0.5276 - acc: 0.8780WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4240 - acc: 0.9095 - val_loss: 0.5240 - val_acc: 0.8782
Learning rate =  9.375e-05
Epoch 29/50
389/390 [============================>.] - ETA: 0s - loss: 0.4154 - acc: 0.9120Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5213 - acc: 0.8790WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4156 - acc: 0.9120 - val_loss: 0.5241 - val_acc: 0.8783
Learning rate =  9.375e-05
Epoch 30/50
389/390 [============================>.] - ETA: 0s - loss: 0.4159 - acc: 0.9124Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5403 - acc: 0.8721WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.4160 - acc: 0.9124 - val_loss: 0.5385 - val_acc: 0.8721
Learning rate =  4.6875e-05
Epoch 31/50
389/390 [============================>.] - ETA: 0s - loss: 0.3993 - acc: 0.9164Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5146 - acc: 0.8754WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 102ms/step - loss: 0.3991 - acc: 0.9165 - val_loss: 0.5157 - val_acc: 0.8761
Learning rate =  4.6875e-05
Epoch 32/50
389/390 [============================>.] - ETA: 0s - loss: 0.3951 - acc: 0.9181Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5113 - acc: 0.8830WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3954 - acc: 0.9179 - val_loss: 0.5147 - val_acc: 0.8834
Learning rate =  4.6875e-05
Epoch 33/50
389/390 [============================>.] - ETA: 0s - loss: 0.3927 - acc: 0.9195Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5154 - acc: 0.8800WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3924 - acc: 0.9196 - val_loss: 0.5146 - val_acc: 0.8806
Learning rate =  4.6875e-05
Epoch 34/50
389/390 [============================>.] - ETA: 0s - loss: 0.3907 - acc: 0.9206Epoch 1/50
 79/390 [=====>........................] - ETA: 24s - loss: 0.5209 - acc: 0.8757WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3906 - acc: 0.9206 - val_loss: 0.5209 - val_acc: 0.8757
Learning rate =  4.6875e-05
Epoch 35/50
389/390 [============================>.] - ETA: 0s - loss: 0.3832 - acc: 0.9214Epoch 1/50
 76/390 [====>.........................] - ETA: 25s - loss: 0.4977 - acc: 0.8816WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3831 - acc: 0.9215 - val_loss: 0.4951 - val_acc: 0.8829
Learning rate =  2.34375e-05
Epoch 36/50
389/390 [============================>.] - ETA: 0s - loss: 0.3775 - acc: 0.9234Epoch 1/50
 79/390 [=====>........................] - ETA: 25s - loss: 0.5019 - acc: 0.8840WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3775 - acc: 0.9234 - val_loss: 0.5019 - val_acc: 0.8840
Learning rate =  2.34375e-05
Epoch 37/50
389/390 [============================>.] - ETA: 0s - loss: 0.3741 - acc: 0.9250Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5026 - acc: 0.8841WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3738 - acc: 0.9250 - val_loss: 0.5053 - val_acc: 0.8847
Learning rate =  2.34375e-05
Epoch 38/50
389/390 [============================>.] - ETA: 0s - loss: 0.3706 - acc: 0.9254Epoch 1/50
 77/390 [====>.........................] - ETA: 26s - loss: 0.5094 - acc: 0.8790WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3707 - acc: 0.9254 - val_loss: 0.5129 - val_acc: 0.8794
Learning rate =  2.34375e-05
Epoch 39/50
389/390 [============================>.] - ETA: 0s - loss: 0.3687 - acc: 0.9259Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5033 - acc: 0.8835WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3686 - acc: 0.9259 - val_loss: 0.5009 - val_acc: 0.8841
Learning rate =  2.34375e-05
Epoch 40/50
389/390 [============================>.] - ETA: 0s - loss: 0.3690 - acc: 0.9258Epoch 1/50
 78/390 [=====>........................] - ETA: 25s - loss: 0.4956 - acc: 0.8860WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3689 - acc: 0.9258 - val_loss: 0.5011 - val_acc: 0.8856
Learning rate =  1.171875e-05
Epoch 41/50
389/390 [============================>.] - ETA: 0s - loss: 0.3613 - acc: 0.9292Epoch 1/50
 78/390 [=====>........................] - ETA: 24s - loss: 0.4987 - acc: 0.8861WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3611 - acc: 0.9292 - val_loss: 0.4977 - val_acc: 0.8861
Learning rate =  1.171875e-05
Epoch 42/50
389/390 [============================>.] - ETA: 0s - loss: 0.3608 - acc: 0.9275Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4909 - acc: 0.8894WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3608 - acc: 0.9275 - val_loss: 0.4911 - val_acc: 0.8896
Learning rate =  1.171875e-05
Epoch 43/50
389/390 [============================>.] - ETA: 0s - loss: 0.3599 - acc: 0.9289Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4854 - acc: 0.8877WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3597 - acc: 0.9290 - val_loss: 0.4826 - val_acc: 0.8883
Learning rate =  1.171875e-05
Epoch 44/50
389/390 [============================>.] - ETA: 0s - loss: 0.3628 - acc: 0.9283Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4963 - acc: 0.8862WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3628 - acc: 0.9283 - val_loss: 0.4985 - val_acc: 0.8866
Learning rate =  1.171875e-05
Epoch 45/50
389/390 [============================>.] - ETA: 0s - loss: 0.3579 - acc: 0.9293Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4926 - acc: 0.8880WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3579 - acc: 0.9293 - val_loss: 0.4927 - val_acc: 0.8882
Learning rate =  5.859375e-06
Epoch 46/50
389/390 [============================>.] - ETA: 0s - loss: 0.3524 - acc: 0.9323Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4881 - acc: 0.8910WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 40s 101ms/step - loss: 0.3525 - acc: 0.9322 - val_loss: 0.4878 - val_acc: 0.8912
Learning rate =  5.859375e-06
Epoch 47/50
389/390 [============================>.] - ETA: 0s - loss: 0.3549 - acc: 0.9315Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.5020 - acc: 0.8841WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3547 - acc: 0.9315 - val_loss: 0.5016 - val_acc: 0.8846
Learning rate =  5.859375e-06
Epoch 48/50
389/390 [============================>.] - ETA: 0s - loss: 0.3540 - acc: 0.9308Epoch 1/50
 79/390 [=====>........................] - ETA: 24s - loss: 0.4932 - acc: 0.8859WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3541 - acc: 0.9307 - val_loss: 0.4932 - val_acc: 0.8859
Learning rate =  5.859375e-06
Epoch 49/50
389/390 [============================>.] - ETA: 0s - loss: 0.3552 - acc: 0.9312Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4714 - acc: 0.8930WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 101ms/step - loss: 0.3550 - acc: 0.9313 - val_loss: 0.4679 - val_acc: 0.8934
Learning rate =  5.859375e-06
Epoch 50/50
389/390 [============================>.] - ETA: 0s - loss: 0.3558 - acc: 0.9298Epoch 1/50
 77/390 [====>.........................] - ETA: 25s - loss: 0.4864 - acc: 0.8872WARNING:tensorflow:Can save best model only with val_accuracy available, skipping.
390/390 [==============================] - 39s 100ms/step - loss: 0.3557 - acc: 0.9299 - val_loss: 0.4840 - val_acc: 0.8873
```
