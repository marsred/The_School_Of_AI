**Training Epochs**

    Train on 60000 samples, validate on 10000 samples
    Epoch 1/20
    
    Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
    60000/60000 [==============================] - 40s 663us/step - loss: 0.1673 - acc: 0.9476 - val_loss: 0.0442 - val_acc: 0.9860
    Epoch 2/20
    
    Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
    60000/60000 [==============================] - 38s 630us/step - loss: 0.0662 - acc: 0.9794 - val_loss: 0.0317 - val_acc: 0.9899
    Epoch 3/20
    
    Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
    60000/60000 [==============================] - 37s 616us/step - loss: 0.0520 - acc: 0.9837 - val_loss: 0.0397 - val_acc: 0.9872
    Epoch 4/20
    
    Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
    60000/60000 [==============================] - 37s 623us/step - loss: 0.0459 - acc: 0.9858 - val_loss: 0.0339 - val_acc: 0.9885
    Epoch 5/20
    
    Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
    60000/60000 [==============================] - 37s 621us/step - loss: 0.0407 - acc: 0.9870 - val_loss: 0.0302 - val_acc: 0.9913
    Epoch 6/20
    
    Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
    60000/60000 [==============================] - 37s 618us/step - loss: 0.0353 - acc: 0.9888 - val_loss: 0.0289 - val_acc: 0.9913
    Epoch 7/20
    
    Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
    60000/60000 [==============================] - 37s 616us/step - loss: 0.0329 - acc: 0.9895 - val_loss: 0.0258 - val_acc: 0.9915
    Epoch 8/20
    
    Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
    60000/60000 [==============================] - 37s 619us/step - loss: 0.0312 - acc: 0.9901 - val_loss: 0.0231 - val_acc: 0.9929
    Epoch 9/20
    
    Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
    60000/60000 [==============================] - 37s 615us/step - loss: 0.0293 - acc: 0.9910 - val_loss: 0.0218 - val_acc: 0.9933
    Epoch 10/20
    
    Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
    60000/60000 [==============================] - 37s 622us/step - loss: 0.0271 - acc: 0.9911 - val_loss: 0.0242 - val_acc: 0.9924
    Epoch 11/20
    
    Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
    60000/60000 [==============================] - 37s 620us/step - loss: 0.0261 - acc: 0.9918 - val_loss: 0.0229 - val_acc: 0.9935
    Epoch 12/20
    
    Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
    60000/60000 [==============================] - 37s 618us/step - loss: 0.0254 - acc: 0.9917 - val_loss: 0.0209 - val_acc: 0.9940
    Epoch 13/20
    
    Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
    60000/60000 [==============================] - 37s 616us/step - loss: 0.0241 - acc: 0.9925 - val_loss: 0.0204 - val_acc: 0.9942
    Epoch 14/20
    
    Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
    60000/60000 [==============================] - 37s 617us/step - loss: 0.0226 - acc: 0.9927 - val_loss: 0.0207 - val_acc: 0.9937
    Epoch 15/20
    
    Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
    60000/60000 [==============================] - 37s 616us/step - loss: 0.0218 - acc: 0.9931 - val_loss: 0.0215 - val_acc: 0.9938
    Epoch 16/20
    
    Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
    60000/60000 [==============================] - 37s 611us/step - loss: 0.0217 - acc: 0.9933 - val_loss: 0.0198 - val_acc: 0.9940
    Epoch 17/20
    
    Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
    60000/60000 [==============================] - 37s 619us/step - loss: 0.0207 - acc: 0.9935 - val_loss: 0.0197 - val_acc: 0.9942
    Epoch 18/20
    
    Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
    60000/60000 [==============================] - 37s 614us/step - loss: 0.0198 - acc: 0.9936 - val_loss: 0.0212 - val_acc: 0.9942
    Epoch 19/20
    
    Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
    60000/60000 [==============================] - 37s 621us/step - loss: 0.0205 - acc: 0.9938 - val_loss: 0.0210 - val_acc: 0.9936
    Epoch 20/20
    
    Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
    60000/60000 [==============================] - 37s 617us/step - loss: 0.0202 - acc: 0.9932 - val_loss: 0.0214 - val_acc: 0.9933
    
    <keras.callbacks.History at 0x7fbf54208e48>

**Model.evaluate**

   

    >>> print(score)
    [0.02138314440062095, 0.9933]


**Strategy**

Initially started the convolution with 10,16 and 32 kernels to fetch as many features as possible till max pooling. After that I used just 16 and 10 kernels to go to the last layer which was of 5 pixels on which I used the 5x5 kernel.
