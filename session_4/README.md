## Assignemnt 4A

- Saved project through online tool (@ ia.inkers.ai)
- [Exported CSV](./via_export_csv.csv)

## [Assignment 4B](Assignment_4B%20(3).ipynb)

Max validation accuracy - `88.090%`

<details>
<summary> 1. Logs </summary>

<p>

```
x_train shape: (50000, 32, 32, 3)
50000 train samples
10000 test samples
y_train shape: (50000, 1)
Model: "model_13"
__________________________________________________________________________________________________
Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_13 (InputLayer)           (None, 32, 32, 3)    0                                            
__________________________________________________________________________________________________
conv2d_253 (Conv2D)             (None, 32, 32, 16)   448         input_13[0][0]                   
__________________________________________________________________________________________________
batch_normalization_229 (BatchN (None, 32, 32, 16)   64          conv2d_253[0][0]                 
__________________________________________________________________________________________________
activation_229 (Activation)     (None, 32, 32, 16)   0           batch_normalization_229[0][0]    
__________________________________________________________________________________________________
conv2d_254 (Conv2D)             (None, 32, 32, 16)   2320        activation_229[0][0]             
__________________________________________________________________________________________________
batch_normalization_230 (BatchN (None, 32, 32, 16)   64          conv2d_254[0][0]                 
__________________________________________________________________________________________________
activation_230 (Activation)     (None, 32, 32, 16)   0           batch_normalization_230[0][0]    
__________________________________________________________________________________________________
conv2d_255 (Conv2D)             (None, 32, 32, 16)   2320        activation_230[0][0]             
__________________________________________________________________________________________________
batch_normalization_231 (BatchN (None, 32, 32, 16)   64          conv2d_255[0][0]                 
__________________________________________________________________________________________________
add_109 (Add)                   (None, 32, 32, 16)   0           activation_229[0][0]             
                                                                 batch_normalization_231[0][0]    
__________________________________________________________________________________________________
activation_231 (Activation)     (None, 32, 32, 16)   0           add_109[0][0]                    
__________________________________________________________________________________________________
conv2d_256 (Conv2D)             (None, 32, 32, 16)   2320        activation_231[0][0]             
__________________________________________________________________________________________________
batch_normalization_232 (BatchN (None, 32, 32, 16)   64          conv2d_256[0][0]                 
__________________________________________________________________________________________________
activation_232 (Activation)     (None, 32, 32, 16)   0           batch_normalization_232[0][0]    
__________________________________________________________________________________________________
conv2d_257 (Conv2D)             (None, 32, 32, 16)   2320        activation_232[0][0]             
__________________________________________________________________________________________________
batch_normalization_233 (BatchN (None, 32, 32, 16)   64          conv2d_257[0][0]                 
__________________________________________________________________________________________________
add_110 (Add)                   (None, 32, 32, 16)   0           activation_231[0][0]             
                                                                 batch_normalization_233[0][0]    
__________________________________________________________________________________________________
activation_233 (Activation)     (None, 32, 32, 16)   0           add_110[0][0]                    
__________________________________________________________________________________________________
conv2d_258 (Conv2D)             (None, 32, 32, 16)   2320        activation_233[0][0]             
__________________________________________________________________________________________________
batch_normalization_234 (BatchN (None, 32, 32, 16)   64          conv2d_258[0][0]                 
__________________________________________________________________________________________________
activation_234 (Activation)     (None, 32, 32, 16)   0           batch_normalization_234[0][0]    
__________________________________________________________________________________________________
conv2d_259 (Conv2D)             (None, 32, 32, 16)   2320        activation_234[0][0]             
__________________________________________________________________________________________________
batch_normalization_235 (BatchN (None, 32, 32, 16)   64          conv2d_259[0][0]                 
__________________________________________________________________________________________________
add_111 (Add)                   (None, 32, 32, 16)   0           activation_233[0][0]             
                                                                 batch_normalization_235[0][0]    
__________________________________________________________________________________________________
activation_235 (Activation)     (None, 32, 32, 16)   0           add_111[0][0]                    
__________________________________________________________________________________________________
conv2d_260 (Conv2D)             (None, 16, 16, 32)   4640        activation_235[0][0]             
__________________________________________________________________________________________________
batch_normalization_236 (BatchN (None, 16, 16, 32)   128         conv2d_260[0][0]                 
__________________________________________________________________________________________________
activation_236 (Activation)     (None, 16, 16, 32)   0           batch_normalization_236[0][0]    
__________________________________________________________________________________________________
conv2d_261 (Conv2D)             (None, 16, 16, 32)   9248        activation_236[0][0]             
__________________________________________________________________________________________________
conv2d_262 (Conv2D)             (None, 16, 16, 32)   544         activation_235[0][0]             
__________________________________________________________________________________________________
batch_normalization_237 (BatchN (None, 16, 16, 32)   128         conv2d_261[0][0]                 
__________________________________________________________________________________________________
add_112 (Add)                   (None, 16, 16, 32)   0           conv2d_262[0][0]                 
                                                                 batch_normalization_237[0][0]    
__________________________________________________________________________________________________
activation_237 (Activation)     (None, 16, 16, 32)   0           add_112[0][0]                    
__________________________________________________________________________________________________
conv2d_263 (Conv2D)             (None, 16, 16, 32)   9248        activation_237[0][0]             
__________________________________________________________________________________________________
batch_normalization_238 (BatchN (None, 16, 16, 32)   128         conv2d_263[0][0]                 
__________________________________________________________________________________________________
activation_238 (Activation)     (None, 16, 16, 32)   0           batch_normalization_238[0][0]    
__________________________________________________________________________________________________
conv2d_264 (Conv2D)             (None, 16, 16, 32)   9248        activation_238[0][0]             
__________________________________________________________________________________________________
batch_normalization_239 (BatchN (None, 16, 16, 32)   128         conv2d_264[0][0]                 
__________________________________________________________________________________________________
add_113 (Add)                   (None, 16, 16, 32)   0           activation_237[0][0]             
                                                                 batch_normalization_239[0][0]    
__________________________________________________________________________________________________
activation_239 (Activation)     (None, 16, 16, 32)   0           add_113[0][0]                    
__________________________________________________________________________________________________
conv2d_265 (Conv2D)             (None, 16, 16, 32)   9248        activation_239[0][0]             
__________________________________________________________________________________________________
batch_normalization_240 (BatchN (None, 16, 16, 32)   128         conv2d_265[0][0]                 
__________________________________________________________________________________________________
activation_240 (Activation)     (None, 16, 16, 32)   0           batch_normalization_240[0][0]    
__________________________________________________________________________________________________
conv2d_266 (Conv2D)             (None, 16, 16, 32)   9248        activation_240[0][0]             
__________________________________________________________________________________________________
batch_normalization_241 (BatchN (None, 16, 16, 32)   128         conv2d_266[0][0]                 
__________________________________________________________________________________________________
add_114 (Add)                   (None, 16, 16, 32)   0           activation_239[0][0]             
                                                                 batch_normalization_241[0][0]    
__________________________________________________________________________________________________
activation_241 (Activation)     (None, 16, 16, 32)   0           add_114[0][0]                    
__________________________________________________________________________________________________
conv2d_267 (Conv2D)             (None, 8, 8, 64)     18496       activation_241[0][0]             
__________________________________________________________________________________________________
batch_normalization_242 (BatchN (None, 8, 8, 64)     256         conv2d_267[0][0]                 
__________________________________________________________________________________________________
activation_242 (Activation)     (None, 8, 8, 64)     0           batch_normalization_242[0][0]    
__________________________________________________________________________________________________
conv2d_268 (Conv2D)             (None, 8, 8, 64)     36928       activation_242[0][0]             
__________________________________________________________________________________________________
conv2d_269 (Conv2D)             (None, 8, 8, 64)     2112        activation_241[0][0]             
__________________________________________________________________________________________________
batch_normalization_243 (BatchN (None, 8, 8, 64)     256         conv2d_268[0][0]                 
__________________________________________________________________________________________________
add_115 (Add)                   (None, 8, 8, 64)     0           conv2d_269[0][0]                 
                                                                 batch_normalization_243[0][0]    
__________________________________________________________________________________________________
activation_243 (Activation)     (None, 8, 8, 64)     0           add_115[0][0]                    
__________________________________________________________________________________________________
conv2d_270 (Conv2D)             (None, 8, 8, 64)     36928       activation_243[0][0]             
__________________________________________________________________________________________________
batch_normalization_244 (BatchN (None, 8, 8, 64)     256         conv2d_270[0][0]                 
__________________________________________________________________________________________________
activation_244 (Activation)     (None, 8, 8, 64)     0           batch_normalization_244[0][0]    
__________________________________________________________________________________________________
conv2d_271 (Conv2D)             (None, 8, 8, 64)     36928       activation_244[0][0]             
__________________________________________________________________________________________________
batch_normalization_245 (BatchN (None, 8, 8, 64)     256         conv2d_271[0][0]                 
__________________________________________________________________________________________________
add_116 (Add)                   (None, 8, 8, 64)     0           activation_243[0][0]             
                                                                 batch_normalization_245[0][0]    
__________________________________________________________________________________________________
activation_245 (Activation)     (None, 8, 8, 64)     0           add_116[0][0]                    
__________________________________________________________________________________________________
conv2d_272 (Conv2D)             (None, 8, 8, 64)     36928       activation_245[0][0]             
__________________________________________________________________________________________________
batch_normalization_246 (BatchN (None, 8, 8, 64)     256         conv2d_272[0][0]                 
__________________________________________________________________________________________________
activation_246 (Activation)     (None, 8, 8, 64)     0           batch_normalization_246[0][0]    
__________________________________________________________________________________________________
conv2d_273 (Conv2D)             (None, 8, 8, 64)     36928       activation_246[0][0]             
__________________________________________________________________________________________________
batch_normalization_247 (BatchN (None, 8, 8, 64)     256         conv2d_273[0][0]                 
__________________________________________________________________________________________________
add_117 (Add)                   (None, 8, 8, 64)     0           activation_245[0][0]             
                                                                 batch_normalization_247[0][0]    
__________________________________________________________________________________________________
activation_247 (Activation)     (None, 8, 8, 64)     0           add_117[0][0]                    
__________________________________________________________________________________________________
average_pooling2d_13 (AveragePo (None, 1, 1, 64)     0           activation_247[0][0]             
__________________________________________________________________________________________________
flatten_13 (Flatten)            (None, 64)           0           average_pooling2d_13[0][0]       
__________________________________________________________________________________________________
dense_13 (Dense)                (None, 10)           650         flatten_13[0][0]                 
==================================================================================================
Total params: 274,442
Trainable params: 273,066
Non-trainable params: 1,376
__________________________________________________________________________________________________
ResNet20v1
Using real-time data augmentation.
Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
1563/1563 [==============================] - 69s 44ms/step - loss: 1.6120 - acc: 0.4763 - val_loss: 1.3781 - val_acc: 0.5744

Epoch 00001: val_acc improved from -inf to 0.57440, saving model to /content/saved_models/cifar10_ResNet20v1_model.001.h5
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0025.
1563/1563 [==============================] - 52s 33ms/step - loss: 1.2042 - acc: 0.6388 - val_loss: 1.5900 - val_acc: 0.5597

Epoch 00002: val_acc did not improve from 0.57440
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.002142857142857143.
1563/1563 [==============================] - 52s 33ms/step - loss: 1.0665 - acc: 0.6917 - val_loss: 1.9710 - val_acc: 0.5088

Epoch 00003: val_acc did not improve from 0.57440
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.001875.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.9771 - acc: 0.7248 - val_loss: 1.4498 - val_acc: 0.6037

Epoch 00004: val_acc improved from 0.57440 to 0.60370, saving model to /content/saved_models/cifar10_ResNet20v1_model.004.h5
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0016666666666666666.
1563/1563 [==============================] - 53s 34ms/step - loss: 0.9108 - acc: 0.7480 - val_loss: 1.1785 - val_acc: 0.6851

Epoch 00005: val_acc improved from 0.60370 to 0.68510, saving model to /content/saved_models/cifar10_ResNet20v1_model.005.h5
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.0015.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.8585 - acc: 0.7643 - val_loss: 0.8832 - val_acc: 0.7537

Epoch 00006: val_acc improved from 0.68510 to 0.75370, saving model to /content/saved_models/cifar10_ResNet20v1_model.006.h5
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0013636363636363635.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.8059 - acc: 0.7822 - val_loss: 1.2650 - val_acc: 0.6703

Epoch 00007: val_acc did not improve from 0.75370
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0012499999999999998.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.7773 - acc: 0.7927 - val_loss: 0.8790 - val_acc: 0.7607

Epoch 00008: val_acc improved from 0.75370 to 0.76070, saving model to /content/saved_models/cifar10_ResNet20v1_model.008.h5
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0011538461538461537.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.7459 - acc: 0.7992 - val_loss: 0.9475 - val_acc: 0.7465

Epoch 00009: val_acc did not improve from 0.76070
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0010714285714285715.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.7226 - acc: 0.8081 - val_loss: 0.9636 - val_acc: 0.7404

Epoch 00010: val_acc did not improve from 0.76070
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.001.
1563/1563 [==============================] - 52s 34ms/step - loss: 0.7002 - acc: 0.8134 - val_loss: 1.0029 - val_acc: 0.7373

Epoch 00011: val_acc did not improve from 0.76070
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.0009375.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.6721 - acc: 0.8262 - val_loss: 0.7608 - val_acc: 0.7980

Epoch 00012: val_acc improved from 0.76070 to 0.79800, saving model to /content/saved_models/cifar10_ResNet20v1_model.012.h5
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.0008823529411764705.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.6531 - acc: 0.8286 - val_loss: 0.8067 - val_acc: 0.7954

Epoch 00013: val_acc did not improve from 0.79800
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.0008333333333333333.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.6366 - acc: 0.8346 - val_loss: 0.7418 - val_acc: 0.8095

Epoch 00014: val_acc improved from 0.79800 to 0.80950, saving model to /content/saved_models/cifar10_ResNet20v1_model.014.h5
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0007894736842105263.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.6186 - acc: 0.8415 - val_loss: 0.7813 - val_acc: 0.7920

Epoch 00015: val_acc did not improve from 0.80950
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.00075.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.6038 - acc: 0.8444 - val_loss: 0.6833 - val_acc: 0.8268

Epoch 00016: val_acc improved from 0.80950 to 0.82680, saving model to /content/saved_models/cifar10_ResNet20v1_model.016.h5
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.0007142857142857143.
1563/1563 [==============================] - 53s 34ms/step - loss: 0.5896 - acc: 0.8488 - val_loss: 0.6678 - val_acc: 0.8319

Epoch 00017: val_acc improved from 0.82680 to 0.83190, saving model to /content/saved_models/cifar10_ResNet20v1_model.017.h5
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0006818181818181818.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5744 - acc: 0.8524 - val_loss: 0.8560 - val_acc: 0.7662

Epoch 00018: val_acc did not improve from 0.83190
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0006521739130434783.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5660 - acc: 0.8541 - val_loss: 0.8345 - val_acc: 0.7961

Epoch 00019: val_acc did not improve from 0.83190
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.0006249999999999999.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5535 - acc: 0.8612 - val_loss: 0.6642 - val_acc: 0.8435

Epoch 00020: val_acc improved from 0.83190 to 0.84350, saving model to /content/saved_models/cifar10_ResNet20v1_model.020.h5
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0006000000000000001.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5409 - acc: 0.8631 - val_loss: 0.6343 - val_acc: 0.8348

Epoch 00021: val_acc did not improve from 0.84350
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.0005769230769230769.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5308 - acc: 0.8648 - val_loss: 0.7701 - val_acc: 0.8025

Epoch 00022: val_acc did not improve from 0.84350
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0005555555555555556.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5256 - acc: 0.8688 - val_loss: 0.6204 - val_acc: 0.8458

Epoch 00023: val_acc improved from 0.84350 to 0.84580, saving model to /content/saved_models/cifar10_ResNet20v1_model.023.h5
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0005357142857142856.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5177 - acc: 0.8690 - val_loss: 0.5842 - val_acc: 0.8518

Epoch 00024: val_acc improved from 0.84580 to 0.85180, saving model to /content/saved_models/cifar10_ResNet20v1_model.024.h5
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.0005172413793103447.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5064 - acc: 0.8725 - val_loss: 0.7693 - val_acc: 0.8099

Epoch 00025: val_acc did not improve from 0.85180
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0005.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.5018 - acc: 0.8740 - val_loss: 0.7342 - val_acc: 0.8095

Epoch 00026: val_acc did not improve from 0.85180
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.0004838709677419355.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4888 - acc: 0.8787 - val_loss: 0.5849 - val_acc: 0.8570

Epoch 00027: val_acc improved from 0.85180 to 0.85700, saving model to /content/saved_models/cifar10_ResNet20v1_model.027.h5
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.00046875.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4876 - acc: 0.8765 - val_loss: 0.6065 - val_acc: 0.8485

Epoch 00028: val_acc did not improve from 0.85700
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.00045454545454545455.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4777 - acc: 0.8788 - val_loss: 0.5527 - val_acc: 0.8628

Epoch 00029: val_acc improved from 0.85700 to 0.86280, saving model to /content/saved_models/cifar10_ResNet20v1_model.029.h5
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.00044117647058823526.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4663 - acc: 0.8847 - val_loss: 0.6373 - val_acc: 0.8386

Epoch 00030: val_acc did not improve from 0.86280
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.0004285714285714286.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4609 - acc: 0.8864 - val_loss: 0.7339 - val_acc: 0.8182

Epoch 00031: val_acc did not improve from 0.86280
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 4.1666666666666665e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.4114 - acc: 0.9023 - val_loss: 0.5288 - val_acc: 0.8731

Epoch 00032: val_acc improved from 0.86280 to 0.87310, saving model to /content/saved_models/cifar10_ResNet20v1_model.032.h5
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 4.054054054054054e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3945 - acc: 0.9085 - val_loss: 0.5154 - val_acc: 0.8780

Epoch 00033: val_acc improved from 0.87310 to 0.87800, saving model to /content/saved_models/cifar10_ResNet20v1_model.033.h5
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 3.9473684210526316e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3901 - acc: 0.9090 - val_loss: 0.5104 - val_acc: 0.8780

Epoch 00034: val_acc did not improve from 0.87800
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 3.846153846153846e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3832 - acc: 0.9122 - val_loss: 0.5105 - val_acc: 0.8774

Epoch 00035: val_acc did not improve from 0.87800
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 3.7500000000000003e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3830 - acc: 0.9126 - val_loss: 0.5011 - val_acc: 0.8798

Epoch 00036: val_acc improved from 0.87800 to 0.87980, saving model to /content/saved_models/cifar10_ResNet20v1_model.036.h5
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 3.658536585365854e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3795 - acc: 0.9129 - val_loss: 0.5076 - val_acc: 0.8766

Epoch 00037: val_acc did not improve from 0.87980
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 3.571428571428572e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3730 - acc: 0.9152 - val_loss: 0.5148 - val_acc: 0.8762

Epoch 00038: val_acc did not improve from 0.87980
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 3.4883720930232556e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3749 - acc: 0.9139 - val_loss: 0.5173 - val_acc: 0.8761

Epoch 00039: val_acc did not improve from 0.87980
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 3.409090909090909e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3709 - acc: 0.9151 - val_loss: 0.5103 - val_acc: 0.8787

Epoch 00040: val_acc did not improve from 0.87980
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 3.3333333333333335e-05.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3685 - acc: 0.9162 - val_loss: 0.5004 - val_acc: 0.8788

Epoch 00041: val_acc did not improve from 0.87980
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 3.260869565217391e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3655 - acc: 0.9178 - val_loss: 0.4950 - val_acc: 0.8809

Epoch 00042: val_acc improved from 0.87980 to 0.88090, saving model to /content/saved_models/cifar10_ResNet20v1_model.042.h5
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 3.191489361702128e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3639 - acc: 0.9181 - val_loss: 0.4969 - val_acc: 0.8798

Epoch 00043: val_acc did not improve from 0.88090
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 3.125e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3656 - acc: 0.9174 - val_loss: 0.5000 - val_acc: 0.8800

Epoch 00044: val_acc did not improve from 0.88090
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 3.0612244897959183e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3654 - acc: 0.9170 - val_loss: 0.4996 - val_acc: 0.8795

Epoch 00045: val_acc did not improve from 0.88090
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 3.000000000000001e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3632 - acc: 0.9177 - val_loss: 0.4984 - val_acc: 0.8797

Epoch 00046: val_acc did not improve from 0.88090
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 2.941176470588235e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3648 - acc: 0.9173 - val_loss: 0.4988 - val_acc: 0.8792

Epoch 00047: val_acc did not improve from 0.88090
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 2.8846153846153846e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3655 - acc: 0.9181 - val_loss: 0.4982 - val_acc: 0.8791

Epoch 00048: val_acc did not improve from 0.88090
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 2.830188679245283e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3630 - acc: 0.9179 - val_loss: 0.5007 - val_acc: 0.8792

Epoch 00049: val_acc did not improve from 0.88090
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 2.777777777777778e-07.
1563/1563 [==============================] - 52s 33ms/step - loss: 0.3638 - acc: 0.9180 - val_loss: 0.4997 - val_acc: 0.8792

Epoch 00050: val_acc did not improve from 0.88090
10000/10000 [==============================] - 2s 200us/step
Test loss: 0.49974792008399965
Test accuracy: 0.8792
```
</p>

</details>
    
3. [GradCAM](./Assignment_4B%20(GradCAM).ipynb)

<details>
<summary> 2. Model </summary>

<p>
​    

```python
from __future__ import print_function
import keras
from keras.layers import Dense, Conv2D, BatchNormalization, Activation
from keras.layers import AveragePooling2D, Input, Flatten
from keras.optimizers import Adam, RMSprop
from keras.callbacks import ModelCheckpoint, LearningRateScheduler
from keras.callbacks import ReduceLROnPlateau
from keras.preprocessing.image import ImageDataGenerator
from keras.regularizers import l2
from keras import backend as K
from keras.models import Model
from keras.datasets import cifar10
import numpy as np
import os

# Training parameters
batch_size = 32  # orig paper trained all networks with batch_size=128
epochs = 50
data_augmentation = True
num_classes = 10

# Subtracting pixel mean improves accuracy
subtract_pixel_mean = True

# Model parameter
# ----------------------------------------------------------------------------
#           |      | 200-epoch | Orig Paper| 200-epoch | Orig Paper| sec/epoch
# Model     |  n   | ResNet v1 | ResNet v1 | ResNet v2 | ResNet v2 | GTX1080Ti
#           |v1(v2)| %Accuracy | %Accuracy | %Accuracy | %Accuracy | v1 (v2)
# ----------------------------------------------------------------------------
# ResNet20  | 3 (2)| 92.16     | 91.25     | -----     | -----     | 35 (---)
# ResNet32  | 5(NA)| 92.46     | 92.49     | NA        | NA        | 50 ( NA)
# ResNet44  | 7(NA)| 92.50     | 92.83     | NA        | NA        | 70 ( NA)
# ResNet56  | 9 (6)| 92.71     | 93.03     | 93.01     | NA        | 90 (100)
# ResNet110 |18(12)| 92.65     | 93.39+-.16| 93.15     | 93.63     | 165(180)
# ResNet164 |27(18)| -----     | 94.07     | -----     | 94.54     | ---(---)
# ResNet1001| (111)| -----     | 92.39     | -----     | 95.08+-.14| ---(---)
# ---------------------------------------------------------------------------
n = 3

# Model version
# Orig paper: version = 1 (ResNet v1), Improved ResNet: version = 2 (ResNet v2)
version = 1

# Computed depth from supplied model parameter n
if version == 1:
    depth = n * 6 + 2
elif version == 2:
    depth = n * 9 + 2

# Model name, depth and version
model_type = 'ResNet%dv%d' % (depth, version)

# Load the CIFAR10 data.
(x_train, y_train), (x_test, y_test) = cifar10.load_data()

# Input image dimensions.
input_shape = x_train.shape[1:]

# Normalize data.
x_train = x_train.astype('float32') / 255
x_test = x_test.astype('float32') / 255

# If subtract pixel mean is enabled
if subtract_pixel_mean:
    x_train_mean = np.mean(x_train, axis=0)
    x_train -= x_train_mean
    x_test -= x_train_mean

print('x_train shape:', x_train.shape)
print(x_train.shape[0], 'train samples')
print(x_test.shape[0], 'test samples')
print('y_train shape:', y_train.shape)

# Convert class vectors to binary class matrices.
y_train = keras.utils.to_categorical(y_train, num_classes)
y_test = keras.utils.to_categorical(y_test, num_classes)


def lr_schedule(epoch):
    """Learning Rate Schedule

    Learning rate is scheduled to be reduced after 80, 120, 160, 180 epochs.
    Called automatically every epoch as part of callbacks during training.

    # Arguments
        epoch (int): The number of epochs

    # Returns
        lr (float32): learning rate
    """
    return 3e-3 / (1 + 0.2 * epoch)


def resnet_layer(inputs,
                 num_filters=16,
                 kernel_size=3,
                 strides=1,
                 activation='relu',
                 batch_normalization=True,
                 conv_first=True):
    """2D Convolution-Batch Normalization-Activation stack builder

    # Arguments
        inputs (tensor): input tensor from input image or previous layer
        num_filters (int): Conv2D number of filters
        kernel_size (int): Conv2D square kernel dimensions
        strides (int): Conv2D square stride dimensions
        activation (string): activation name
        batch_normalization (bool): whether to include batch normalization
        conv_first (bool): conv-bn-activation (True) or
            bn-activation-conv (False)

    # Returns
        x (tensor): tensor as input to the next layer
    """
    conv = Conv2D(num_filters,
                  kernel_size=kernel_size,
                  strides=strides,
                  padding='same',
                  kernel_initializer='he_normal',
                  kernel_regularizer=l2(1e-4))

    x = inputs
    if conv_first:
        x = conv(x)
        if batch_normalization:
            x = BatchNormalization()(x)
        if activation is not None:
            x = Activation(activation)(x)
    else:
        if batch_normalization:
            x = BatchNormalization()(x)
        if activation is not None:
            x = Activation(activation)(x)
        x = conv(x)
    return x


def resnet_v1(input_shape, depth, num_classes=10):
    """ResNet Version 1 Model builder [a]

    Stacks of 2 x (3 x 3) Conv2D-BN-ReLU
    Last ReLU is after the shortcut connection.
    At the beginning of each stage, the feature map size is halved (downsampled)
    by a convolutional layer with strides=2, while the number of filters is
    doubled. Within each stage, the layers have the same number filters and the
    same number of filters.
    Features maps sizes:
    stage 0: 32x32, 16
    stage 1: 16x16, 32
    stage 2:  8x8,  64
    The Number of parameters is approx the same as Table 6 of [a]:
    ResNet20 0.27M
    ResNet32 0.46M
    ResNet44 0.66M
    ResNet56 0.85M
    ResNet110 1.7M

    # Arguments
        input_shape (tensor): shape of input image tensor
        depth (int): number of core convolutional layers
        num_classes (int): number of classes (CIFAR10 has 10)

    # Returns
        model (Model): Keras model instance
    """
    if (depth - 2) % 6 != 0:
        raise ValueError('depth should be 6n+2 (eg 20, 32, 44 in [a])')
    # Start model definition.
    num_filters = 16
    num_res_blocks = int((depth - 2) / 6)

    inputs = Input(shape=input_shape)
    x = resnet_layer(inputs=inputs)
    # Instantiate the stack of residual units
    for stack in range(3):
        for res_block in range(num_res_blocks):
            strides = 1
            if stack > 0 and res_block == 0:  # first layer but not first stack
                strides = 2  # downsample
            y = resnet_layer(inputs=x,
                             num_filters=num_filters,
                             strides=strides)
            y = resnet_layer(inputs=y,
                             num_filters=num_filters,
                             activation=None)
            if stack > 0 and res_block == 0:  # first layer but not first stack
                # linear projection residual shortcut connection to match
                # changed dims
                x = resnet_layer(inputs=x,
                                 num_filters=num_filters,
                                 kernel_size=1,
                                 strides=strides,
                                 activation=None,
                                 batch_normalization=False)
            x = keras.layers.add([x, y])
            x = Activation('relu')(x)
        num_filters *= 2

    # Add classifier on top.
    # v1 does not use BN after last shortcut connection-ReLU
    x = AveragePooling2D(pool_size=8)(x)
    y = Flatten()(x)
    outputs = Dense(num_classes,
                    activation='softmax',
                    kernel_initializer='he_normal')(y)

    # Instantiate model.
    model = Model(inputs=inputs, outputs=outputs)
    return model


def resnet_v2(input_shape, depth, num_classes=10):
    """ResNet Version 2 Model builder [b]

    Stacks of (1 x 1)-(3 x 3)-(1 x 1) BN-ReLU-Conv2D or also known as
    bottleneck layer
    First shortcut connection per layer is 1 x 1 Conv2D.
    Second and onwards shortcut connection is identity.
    At the beginning of each stage, the feature map size is halved (downsampled)
    by a convolutional layer with strides=2, while the number of filter maps is
    doubled. Within each stage, the layers have the same number filters and the
    same filter map sizes.
    Features maps sizes:
    conv1  : 32x32,  16
    stage 0: 32x32,  64
    stage 1: 16x16, 128
    stage 2:  8x8,  256

    # Arguments
        input_shape (tensor): shape of input image tensor
        depth (int): number of core convolutional layers
        num_classes (int): number of classes (CIFAR10 has 10)

    # Returns
        model (Model): Keras model instance
    """
    if (depth - 2) % 9 != 0:
        raise ValueError('depth should be 9n+2 (eg 56 or 110 in [b])')
    # Start model definition.
    num_filters_in = 16
    num_res_blocks = int((depth - 2) / 9)

    inputs = Input(shape=input_shape)
    # v2 performs Conv2D with BN-ReLU on input before splitting into 2 paths
    x = resnet_layer(inputs=inputs,
                     num_filters=num_filters_in,
                     conv_first=True)

    # Instantiate the stack of residual units
    for stage in range(3):
        for res_block in range(num_res_blocks):
            activation = 'relu'
            batch_normalization = True
            strides = 1
            if stage == 0:
                num_filters_out = num_filters_in * 4
                if res_block == 0:  # first layer and first stage
                    activation = None
                    batch_normalization = False
            else:
                num_filters_out = num_filters_in * 2
                if res_block == 0:  # first layer but not first stage
                    strides = 2    # downsample

            # bottleneck residual unit
            y = resnet_layer(inputs=x,
                             num_filters=num_filters_in,
                             kernel_size=1,
                             strides=strides,
                             activation=activation,
                             batch_normalization=batch_normalization,
                             conv_first=False)
            y = resnet_layer(inputs=y,
                             num_filters=num_filters_in,
                             conv_first=False)
            y = resnet_layer(inputs=y,
                             num_filters=num_filters_out,
                             kernel_size=1,
                             conv_first=False)
            if res_block == 0:
                # linear projection residual shortcut connection to match
                # changed dims
                x = resnet_layer(inputs=x,
                                 num_filters=num_filters_out,
                                 kernel_size=1,
                                 strides=strides,
                                 activation=None,
                                 batch_normalization=False)
            x = keras.layers.add([x, y])

        num_filters_in = num_filters_out

    # Add classifier on top.
    # v2 has BN-ReLU before Pooling
    x = BatchNormalization()(x)
    x = Activation('relu')(x)
    x = AveragePooling2D(pool_size=8)(x)
    y = Flatten()(x)
    outputs = Dense(num_classes,
                    activation='softmax',
                    kernel_initializer='he_normal')(y)

    # Instantiate model.
    model = Model(inputs=inputs, outputs=outputs)
    return model


def get_random_eraser(p=0.5, s_l=0.02, s_h=0.4, r_1=0.3, r_2=1/0.3, v_l=0, v_h=255):
    def eraser(input_img):
        img_h, img_w, _ = input_img.shape
        p_1 = np.random.rand()

        if p_1 > p:
            return input_img

        while True:
            s = np.random.uniform(s_l, s_h) * img_h * img_w
            r = np.random.uniform(r_1, r_2)
            w = int(np.sqrt(s / r))
            h = int(np.sqrt(s * r))
            left = np.random.randint(0, img_w)
            top = np.random.randint(0, img_h)

            if left + w <= img_w and top + h <= img_h:
                break

        c = np.random.uniform(v_l, v_h)
        input_img[top:top + h, left:left + w, :] = c

        return input_img

    return eraser


if version == 2:
    model = resnet_v2(input_shape=input_shape, depth=depth)
else:
    model = resnet_v1(input_shape=input_shape, depth=depth)

model.compile(loss='categorical_crossentropy',
              optimizer=RMSprop(lr=3e-3),
              metrics=['accuracy'])
model.summary()
print(model_type)

# Prepare model model saving directory.
save_dir = os.path.join(os.getcwd(), 'saved_models')
model_name = 'cifar10_%s_model.{epoch:03d}.h5' % model_type
if not os.path.isdir(save_dir):
    os.makedirs(save_dir)
filepath = os.path.join(save_dir, model_name)

# Prepare callbacks for model saving and for learning rate adjustment.
checkpoint = ModelCheckpoint(filepath=filepath,
                             monitor='val_acc',
                             verbose=1,
                             save_best_only=True)

lr_scheduler = LearningRateScheduler(lr_schedule)

lr_reducer = ReduceLROnPlateau(factor=np.sqrt(0.1),
                               cooldown=0,
                               patience=5,
                               min_lr=0.5e-6)

callbacks = [checkpoint, lr_reducer, lr_scheduler]

print('Using real-time data augmentation.')
# This will do preprocessing and realtime data augmentation:
datagen = ImageDataGenerator(
    width_shift_range=0.1,
    # height_shift_range=0.1,
    horizontal_flip=True,
    # vertical_flip=True, 
    zoom_range=0.1,
    rotation_range=10,
    # shear_range=10,
    fill_mode='nearest',
    preprocessing_function=get_random_eraser(v_l=0, v_h=1, p=0.1),
)

# Compute quantities required for featurewise normalization
# (std, mean, and principal components if ZCA whitening is applied).
datagen.fit(x_train)

# Fit the model on the batches generated by datagen.flow().
model.fit_generator(datagen.flow(x_train, y_train, batch_size=batch_size),
                    validation_data=(x_test, y_test),
                    epochs=epochs, verbose=1, workers=4,
                    callbacks=callbacks)

# Score trained model.
scores = model.evaluate(x_test, y_test, verbose=1)
print('Test loss:', scores[0])
print('Test accuracy:', scores[1])
```


</p>
    
</details>
