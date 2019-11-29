## Session 2

### [Training logs](./session_2.ipynb)

Max accuracy - `99.46`

```
Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 45s 750us/step - loss: 0.5764 - acc: 0.8631 - val_loss: 0.1597 - val_acc: 0.9759
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.002.
60000/60000 [==============================] - 10s 163us/step - loss: 0.2237 - acc: 0.9558 - val_loss: 0.0875 - val_acc: 0.9857
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0015.
60000/60000 [==============================] - 10s 159us/step - loss: 0.1766 - acc: 0.9649 - val_loss: 0.0816 - val_acc: 0.9872
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0012000000000000001.
60000/60000 [==============================] - 10s 159us/step - loss: 0.1480 - acc: 0.9700 - val_loss: 0.0594 - val_acc: 0.9879
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.001.
60000/60000 [==============================] - 10s 165us/step - loss: 0.1347 - acc: 0.9723 - val_loss: 0.0520 - val_acc: 0.9912
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0008571428571428572.
60000/60000 [==============================] - 10s 165us/step - loss: 0.1242 - acc: 0.9741 - val_loss: 0.0410 - val_acc: 0.9912
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.00075.
60000/60000 [==============================] - 10s 164us/step - loss: 0.1114 - acc: 0.9767 - val_loss: 0.0381 - val_acc: 0.9922
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0006666666666666666.
60000/60000 [==============================] - 10s 163us/step - loss: 0.1062 - acc: 0.9778 - val_loss: 0.0334 - val_acc: 0.9922
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0006000000000000001.
60000/60000 [==============================] - 10s 161us/step - loss: 0.1005 - acc: 0.9789 - val_loss: 0.0366 - val_acc: 0.9920
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0005454545454545455.
60000/60000 [==============================] - 10s 161us/step - loss: 0.0938 - acc: 0.9798 - val_loss: 0.0303 - val_acc: 0.9928
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0005.
60000/60000 [==============================] - 10s 162us/step - loss: 0.0899 - acc: 0.9807 - val_loss: 0.0334 - val_acc: 0.9918
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.00046153846153846153.
60000/60000 [==============================] - 10s 162us/step - loss: 0.0863 - acc: 0.9810 - val_loss: 0.0314 - val_acc: 0.9926
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0004285714285714286.
60000/60000 [==============================] - 10s 163us/step - loss: 0.0838 - acc: 0.9807 - val_loss: 0.0274 - val_acc: 0.9931
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0004.
60000/60000 [==============================] - 10s 159us/step - loss: 0.0810 - acc: 0.9811 - val_loss: 0.0258 - val_acc: 0.9946
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.000375.
60000/60000 [==============================] - 10s 158us/step - loss: 0.0771 - acc: 0.9813 - val_loss: 0.0254 - val_acc: 0.9940
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.00035294117647058826.
60000/60000 [==============================] - 10s 159us/step - loss: 0.0767 - acc: 0.9817 - val_loss: 0.0235 - val_acc: 0.9941
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.0003333333333333333.
60000/60000 [==============================] - 10s 160us/step - loss: 0.0723 - acc: 0.9823 - val_loss: 0.0248 - val_acc: 0.9939
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.00031578947368421053.
60000/60000 [==============================] - 10s 159us/step - loss: 0.0710 - acc: 0.9831 - val_loss: 0.0240 - val_acc: 0.9937
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.00030000000000000003.
60000/60000 [==============================] - 9s 158us/step - loss: 0.0679 - acc: 0.9842 - val_loss: 0.0241 - val_acc: 0.9937
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.00028571428571428574.
60000/60000 [==============================] - 9s 157us/step - loss: 0.0667 - acc: 0.9828 - val_loss: 0.0238 - val_acc: 0.9939
```

Evaluation Result -

```
>>> model.evaluate(test_images, test_labels)
[0.023790680991858243, 0.9939]
```


### General strategy 

1. Created model with 2 MaxPooling layers, and 1 Dense layer at end. Trained with default learning rate.
2. Observed large difference between training and validation accuracy, so applied 2 dropout layers.
3. Trained for 20 epochs, but not achieved required accuracy, so trained for 40 epochs.
4. Tweaked training rate to get required accuracy within 20 epochs.
5. Still not getting required accuracy, so used only 1 MaxPooling layer, and removed all Dense layers. (as seen in 8th Dnn)
6. Added dropout layers after each Conv2D layer. (as seen in 8th Dnn)
7. Success!