# Person Attribute:

## Parameters : 

```
Total params: 21,550,555
Trainable params: 21,543,387
Non-trainable params: 7,168
```

## Model :

```
Model: "model_1"
__________________________________________________________________________________________________
Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_1 (InputLayer)            (None, 224, 224, 3)  0                                            
__________________________________________________________________________________________________
block1_conv1 (Conv2D)           (None, 224, 224, 64) 1792        input_1[0][0]                    
__________________________________________________________________________________________________
block1_conv2 (Conv2D)           (None, 224, 224, 64) 36928       block1_conv1[0][0]               
__________________________________________________________________________________________________
block1_pool (MaxPooling2D)      (None, 112, 112, 64) 0           block1_conv2[0][0]               
__________________________________________________________________________________________________
block2_conv1 (Conv2D)           (None, 112, 112, 128 73856       block1_pool[0][0]                
__________________________________________________________________________________________________
block2_conv2 (Conv2D)           (None, 112, 112, 128 147584      block2_conv1[0][0]               
__________________________________________________________________________________________________
block2_pool (MaxPooling2D)      (None, 56, 56, 128)  0           block2_conv2[0][0]               
__________________________________________________________________________________________________
block3_conv1 (Conv2D)           (None, 56, 56, 256)  295168      block2_pool[0][0]                
__________________________________________________________________________________________________
block3_conv2 (Conv2D)           (None, 56, 56, 256)  590080      block3_conv1[0][0]               
__________________________________________________________________________________________________
block3_conv3 (Conv2D)           (None, 56, 56, 256)  590080      block3_conv2[0][0]               
__________________________________________________________________________________________________
block3_pool (MaxPooling2D)      (None, 28, 28, 256)  0           block3_conv3[0][0]               
__________________________________________________________________________________________________
block4_conv1 (Conv2D)           (None, 28, 28, 512)  1180160     block3_pool[0][0]                
__________________________________________________________________________________________________
block4_conv2 (Conv2D)           (None, 28, 28, 512)  2359808     block4_conv1[0][0]               
__________________________________________________________________________________________________
block4_conv3 (Conv2D)           (None, 28, 28, 512)  2359808     block4_conv2[0][0]               
__________________________________________________________________________________________________
block4_pool (MaxPooling2D)      (None, 14, 14, 512)  0           block4_conv3[0][0]               
__________________________________________________________________________________________________
block5_conv1 (Conv2D)           (None, 14, 14, 512)  2359808     block4_pool[0][0]                
__________________________________________________________________________________________________
block5_conv2 (Conv2D)           (None, 14, 14, 512)  2359808     block5_conv1[0][0]               
__________________________________________________________________________________________________
block5_conv3 (Conv2D)           (None, 14, 14, 512)  2359808     block5_conv2[0][0]               
__________________________________________________________________________________________________
block5_pool (MaxPooling2D)      (None, 7, 7, 512)    0           block5_conv3[0][0]               
__________________________________________________________________________________________________
batch_normalization_1 (BatchNor (None, 7, 7, 512)    2048        block5_pool[0][0]                
__________________________________________________________________________________________________
flatten (Flatten)               (None, 25088)        0           batch_normalization_1[0][0]      
__________________________________________________________________________________________________
dense_1 (Dense)                 (None, 256)          6422784     flatten[0][0]                    
__________________________________________________________________________________________________
dropout_1 (Dropout)             (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_3 (Dropout)             (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_5 (Dropout)             (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_7 (Dropout)             (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_9 (Dropout)             (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_11 (Dropout)            (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_15 (Dropout)            (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
dropout_13 (Dropout)            (None, 256)          0           dense_1[0][0]                    
__________________________________________________________________________________________________
batch_normalization_2 (BatchNor (None, 256)          1024        dropout_1[0][0]                  
__________________________________________________________________________________________________
batch_normalization_4 (BatchNor (None, 256)          1024        dropout_3[0][0]                  
__________________________________________________________________________________________________
batch_normalization_6 (BatchNor (None, 256)          1024        dropout_5[0][0]                  
__________________________________________________________________________________________________
batch_normalization_8 (BatchNor (None, 256)          1024        dropout_7[0][0]                  
__________________________________________________________________________________________________
batch_normalization_10 (BatchNo (None, 256)          1024        dropout_9[0][0]                  
__________________________________________________________________________________________________
batch_normalization_12 (BatchNo (None, 256)          1024        dropout_11[0][0]                 
__________________________________________________________________________________________________
batch_normalization_16 (BatchNo (None, 256)          1024        dropout_15[0][0]                 
__________________________________________________________________________________________________
batch_normalization_14 (BatchNo (None, 256)          1024        dropout_13[0][0]                 
__________________________________________________________________________________________________
dense_2 (Dense)                 (None, 128)          32896       batch_normalization_2[0][0]      
__________________________________________________________________________________________________
dense_4 (Dense)                 (None, 128)          32896       batch_normalization_4[0][0]      
__________________________________________________________________________________________________
dense_6 (Dense)                 (None, 128)          32896       batch_normalization_6[0][0]      
__________________________________________________________________________________________________
dense_8 (Dense)                 (None, 128)          32896       batch_normalization_8[0][0]      
__________________________________________________________________________________________________
dense_10 (Dense)                (None, 128)          32896       batch_normalization_10[0][0]     
__________________________________________________________________________________________________
dense_12 (Dense)                (None, 128)          32896       batch_normalization_12[0][0]     
__________________________________________________________________________________________________
dense_16 (Dense)                (None, 128)          32896       batch_normalization_16[0][0]     
__________________________________________________________________________________________________
dense_14 (Dense)                (None, 128)          32896       batch_normalization_14[0][0]     
__________________________________________________________________________________________________
dropout_2 (Dropout)             (None, 128)          0           dense_2[0][0]                    
__________________________________________________________________________________________________
dropout_4 (Dropout)             (None, 128)          0           dense_4[0][0]                    
__________________________________________________________________________________________________
dropout_6 (Dropout)             (None, 128)          0           dense_6[0][0]                    
__________________________________________________________________________________________________
dropout_8 (Dropout)             (None, 128)          0           dense_8[0][0]                    
__________________________________________________________________________________________________
dropout_10 (Dropout)            (None, 128)          0           dense_10[0][0]                   
__________________________________________________________________________________________________
dropout_12 (Dropout)            (None, 128)          0           dense_12[0][0]                   
__________________________________________________________________________________________________
dropout_16 (Dropout)            (None, 128)          0           dense_16[0][0]                   
__________________________________________________________________________________________________
dropout_14 (Dropout)            (None, 128)          0           dense_14[0][0]                   
__________________________________________________________________________________________________
batch_normalization_3 (BatchNor (None, 128)          512         dropout_2[0][0]                  
__________________________________________________________________________________________________
batch_normalization_5 (BatchNor (None, 128)          512         dropout_4[0][0]                  
__________________________________________________________________________________________________
batch_normalization_7 (BatchNor (None, 128)          512         dropout_6[0][0]                  
__________________________________________________________________________________________________
batch_normalization_9 (BatchNor (None, 128)          512         dropout_8[0][0]                  
__________________________________________________________________________________________________
batch_normalization_11 (BatchNo (None, 128)          512         dropout_10[0][0]                 
__________________________________________________________________________________________________
batch_normalization_13 (BatchNo (None, 128)          512         dropout_12[0][0]                 
__________________________________________________________________________________________________
batch_normalization_17 (BatchNo (None, 128)          512         dropout_16[0][0]                 
__________________________________________________________________________________________________
batch_normalization_15 (BatchNo (None, 128)          512         dropout_14[0][0]                 
__________________________________________________________________________________________________
dense_3 (Dense)                 (None, 128)          16512       batch_normalization_3[0][0]      
__________________________________________________________________________________________________
dense_5 (Dense)                 (None, 128)          16512       batch_normalization_5[0][0]      
__________________________________________________________________________________________________
dense_7 (Dense)                 (None, 128)          16512       batch_normalization_7[0][0]      
__________________________________________________________________________________________________
dense_9 (Dense)                 (None, 128)          16512       batch_normalization_9[0][0]      
__________________________________________________________________________________________________
dense_11 (Dense)                (None, 128)          16512       batch_normalization_11[0][0]     
__________________________________________________________________________________________________
dense_13 (Dense)                (None, 128)          16512       batch_normalization_13[0][0]     
__________________________________________________________________________________________________
dense_17 (Dense)                (None, 128)          16512       batch_normalization_17[0][0]     
__________________________________________________________________________________________________
dense_15 (Dense)                (None, 128)          16512       batch_normalization_15[0][0]     
__________________________________________________________________________________________________
gender_output (Dense)           (None, 2)            258         dense_3[0][0]                    
__________________________________________________________________________________________________
image_quality_output (Dense)    (None, 3)            387         dense_5[0][0]                    
__________________________________________________________________________________________________
age_output (Dense)              (None, 5)            645         dense_7[0][0]                    
__________________________________________________________________________________________________
weight_output (Dense)           (None, 4)            516         dense_9[0][0]                    
__________________________________________________________________________________________________
bag_output (Dense)              (None, 3)            387         dense_11[0][0]                   
__________________________________________________________________________________________________
footwear_output (Dense)         (None, 3)            387         dense_13[0][0]                   
__________________________________________________________________________________________________
pose_output (Dense)             (None, 3)            387         dense_17[0][0]                   
__________________________________________________________________________________________________
emotion_output (Dense)          (None, 4)            516         dense_15[0][0]                   
==================================================================================================
Total params: 21,550,555
Trainable params: 21,543,387
Non-trainable params: 7,168
__________________________________________________________________________________________________
```



## Best Accuracy : 

```
360/360 [==============================] - 51s 142ms/step
- loss: 2.2692 
- gender_output_loss: 0.1436 
- image_quality_output_loss: 0.3243 
- age_output_loss: 0.3663 
- weight_output_loss: 0.3069 
- bag_output_loss: 0.2804 
- footwear_output_loss: 0.2759 
- pose_output_loss: 0.1818 
- emotion_output_loss: 0.2801 
- gender_output_acc: 0.9402 
- image_quality_output_acc: 0.8760 
- age_output_acc: 0.8655 
- weight_output_acc: 0.8886 
- bag_output_acc: 0.8944 
- footwear_output_acc: 0.8934 
- pose_output_acc: 0.9318 
- emotion_output_acc: 0.9063 
- val_loss: 11.0289 
- val_gender_output_loss: 0.5063 
- val_image_quality_output_loss: 1.4282 
- val_age_output_loss: 2.3395 
- val_weight_output_loss: 1.4962 
- val_bag_output_loss: 1.2897 
- val_footwear_output_loss: 1.1025 
- val_pose_output_loss: 0.7405 
- val_emotion_output_loss: 1.4243 
- val_gender_output_acc: 0.8286 
- val_image_quality_output_acc: 0.5247 
- val_age_output_acc: 0.3574 
- val_weight_output_acc: 0.5610 
- val_bag_output_acc: 0.5897 
- val_footwear_output_acc: 0.6472 
- val_pose_output_acc: 0.7797 
- val_emotion_output_acc: 0.6386
```

# Evaluated Result:

Final Evaluated result on the model for the validatation data result 

```
[11.052993097612935,
 0.5063016563653946,
 1.4301760408186144,
 2.350307191571882,
 1.5013189777251212,
 1.2914905125094998,
 1.1030988693237305,
 0.7409410813162404,
 1.4242667478899802,
 0.827116935483871,
 0.5216733870967742,
 0.35735887096774194,
 0.5569556451612904,
 0.5871975806451613,
 0.6456653225806451,
 0.7792338709677419,
 0.6391129032258065]
 ```
