**Final Validation accuracy for Base Network:** 82.99%

**My Model definition:**

    model = Sequential()
    model.add(SeparableConv2D(48, 3, padding='same', input_shape=(32, 32, 3))) # 32, RF: 3
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(SeparableConv2D(96, 3)) # 30, RF: 5
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(SeparableConv2D(192, 3)) # 28, RF: 7
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(MaxPooling2D(pool_size=(2, 2))) # 14, RF: 9
    model.add(Dropout(0.1))
    
    model.add(SeparableConv2D(96, 3, padding='same')) # 14, RF: 17
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(SeparableConv2D(96, 3)) # 12, RF: 25
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(SeparableConv2D(96, 3)) # 10, RF: 33
    model.add(Activation('relu'))
    model.add(BatchNormalization())
    model.add(Dropout(0.1))
    
    model.add(MaxPooling2D(pool_size=(2, 2))) # 5, RF: 41
    model.add(Dropout(0.1))
    
    model.add(GlobalAveragePooling2D())
    model.add(Dense(256))
    model.add(Activation('relu'))
    model.add(Dropout(0.2))
    model.add(Dense(num_classes, activation='softmax'))

**Training Log:**

    Epoch 1/50
    
    Epoch 00001: LearningRateScheduler setting learning rate to 0.004.
    390/390 [==============================] - 31s 79ms/step - loss: 1.4738 - acc: 0.4647 - val_loss: 1.7124 - val_acc: 0.4816
    Epoch 2/50
    
    Epoch 00002: LearningRateScheduler setting learning rate to 0.0033333333.
    390/390 [==============================] - 28s 71ms/step - loss: 1.1116 - acc: 0.6066 - val_loss: 1.1940 - val_acc: 0.6154
    Epoch 3/50
    
    Epoch 00003: LearningRateScheduler setting learning rate to 0.0028571429.
    390/390 [==============================] - 28s 71ms/step - loss: 0.9662 - acc: 0.6589 - val_loss: 1.0737 - val_acc: 0.6488
    Epoch 4/50
    
    Epoch 00004: LearningRateScheduler setting learning rate to 0.0025.
    390/390 [==============================] - 28s 71ms/step - loss: 0.8824 - acc: 0.6900 - val_loss: 0.9888 - val_acc: 0.6865
    Epoch 5/50
    
    Epoch 00005: LearningRateScheduler setting learning rate to 0.0022222222.
    390/390 [==============================] - 28s 71ms/step - loss: 0.8262 - acc: 0.7119 - val_loss: 0.8875 - val_acc: 0.7108
    Epoch 6/50
    
    Epoch 00006: LearningRateScheduler setting learning rate to 0.002.
    390/390 [==============================] - 28s 71ms/step - loss: 0.7708 - acc: 0.7313 - val_loss: 0.8688 - val_acc: 0.7221
    Epoch 7/50
    
    Epoch 00007: LearningRateScheduler setting learning rate to 0.0018181818.
    390/390 [==============================] - 28s 71ms/step - loss: 0.7378 - acc: 0.7414 - val_loss: 0.8558 - val_acc: 0.7317
    Epoch 8/50
    
    Epoch 00008: LearningRateScheduler setting learning rate to 0.0016666667.
    390/390 [==============================] - 28s 71ms/step - loss: 0.7102 - acc: 0.7546 - val_loss: 0.7232 - val_acc: 0.7619
    Epoch 9/50
    
    Epoch 00009: LearningRateScheduler setting learning rate to 0.0015384615.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6853 - acc: 0.7605 - val_loss: 0.7846 - val_acc: 0.7521
    Epoch 10/50
    
    Epoch 00010: LearningRateScheduler setting learning rate to 0.0014285714.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6620 - acc: 0.7696 - val_loss: 0.6679 - val_acc: 0.7833
    Epoch 11/50
    
    Epoch 00011: LearningRateScheduler setting learning rate to 0.0013333333.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6451 - acc: 0.7756 - val_loss: 0.6599 - val_acc: 0.7857
    Epoch 12/50
    
    Epoch 00012: LearningRateScheduler setting learning rate to 0.00125.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6284 - acc: 0.7807 - val_loss: 0.6361 - val_acc: 0.7944
    Epoch 13/50
    
    Epoch 00013: LearningRateScheduler setting learning rate to 0.0011764706.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6150 - acc: 0.7847 - val_loss: 0.6456 - val_acc: 0.7891
    Epoch 14/50
    
    Epoch 00014: LearningRateScheduler setting learning rate to 0.0011111111.
    390/390 [==============================] - 28s 71ms/step - loss: 0.6002 - acc: 0.7905 - val_loss: 0.6878 - val_acc: 0.7895
    Epoch 15/50
    
    Epoch 00015: LearningRateScheduler setting learning rate to 0.0010526316.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5898 - acc: 0.7956 - val_loss: 0.7240 - val_acc: 0.7787
    Epoch 16/50
    
    Epoch 00016: LearningRateScheduler setting learning rate to 0.001.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5798 - acc: 0.7981 - val_loss: 0.6187 - val_acc: 0.8045
    Epoch 17/50
    
    Epoch 00017: LearningRateScheduler setting learning rate to 0.000952381.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5655 - acc: 0.8023 - val_loss: 0.5889 - val_acc: 0.8123
    Epoch 18/50
    
    Epoch 00018: LearningRateScheduler setting learning rate to 0.0009090909.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5585 - acc: 0.8045 - val_loss: 0.6637 - val_acc: 0.7896
    Epoch 19/50
    
    Epoch 00019: LearningRateScheduler setting learning rate to 0.0008695652.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5558 - acc: 0.8045 - val_loss: 0.6288 - val_acc: 0.8050
    Epoch 20/50
    
    Epoch 00020: LearningRateScheduler setting learning rate to 0.0008333333.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5504 - acc: 0.8086 - val_loss: 0.6194 - val_acc: 0.8071
    Epoch 21/50
    
    Epoch 00021: LearningRateScheduler setting learning rate to 0.0008.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5342 - acc: 0.8136 - val_loss: 0.5548 - val_acc: 0.8221
    Epoch 22/50
    
    Epoch 00022: LearningRateScheduler setting learning rate to 0.0007692308.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5309 - acc: 0.8143 - val_loss: 0.5809 - val_acc: 0.8163
    Epoch 23/50
    
    Epoch 00023: LearningRateScheduler setting learning rate to 0.0007407407.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5251 - acc: 0.8160 - val_loss: 0.5665 - val_acc: 0.8178
    Epoch 24/50
    
    Epoch 00024: LearningRateScheduler setting learning rate to 0.0007142857.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5183 - acc: 0.8190 - val_loss: 0.6246 - val_acc: 0.8069
    Epoch 25/50
    
    Epoch 00025: LearningRateScheduler setting learning rate to 0.0006896552.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5089 - acc: 0.8221 - val_loss: 0.5870 - val_acc: 0.8132
    Epoch 26/50
    
    Epoch 00026: LearningRateScheduler setting learning rate to 0.0006666667.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5060 - acc: 0.8226 - val_loss: 0.6433 - val_acc: 0.8034
    Epoch 27/50
    
    Epoch 00027: LearningRateScheduler setting learning rate to 0.0006451613.
    390/390 [==============================] - 28s 71ms/step - loss: 0.5046 - acc: 0.8257 - val_loss: 0.5804 - val_acc: 0.8181
    Epoch 28/50
    
    Epoch 00028: LearningRateScheduler setting learning rate to 0.000625.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4913 - acc: 0.8294 - val_loss: 0.5828 - val_acc: 0.8180
    Epoch 29/50
    
    Epoch 00029: LearningRateScheduler setting learning rate to 0.0006060606.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4941 - acc: 0.8276 - val_loss: 0.5590 - val_acc: 0.8222
    Epoch 30/50
    
    Epoch 00030: LearningRateScheduler setting learning rate to 0.0005882353.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4836 - acc: 0.8317 - val_loss: 0.5863 - val_acc: 0.8170
    Epoch 31/50
    
    Epoch 00031: LearningRateScheduler setting learning rate to 0.0005714286.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4804 - acc: 0.8302 - val_loss: 0.5400 - val_acc: 0.8283
    Epoch 32/50
    
    Epoch 00032: LearningRateScheduler setting learning rate to 0.0005555556.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4844 - acc: 0.8308 - val_loss: 0.5622 - val_acc: 0.8261
    Epoch 33/50
    
    Epoch 00033: LearningRateScheduler setting learning rate to 0.0005405405.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4808 - acc: 0.8324 - val_loss: 0.5464 - val_acc: 0.8243
    Epoch 34/50
    
    Epoch 00034: LearningRateScheduler setting learning rate to 0.0005263158.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4730 - acc: 0.8349 - val_loss: 0.5655 - val_acc: 0.8236
    Epoch 35/50
    
    Epoch 00035: LearningRateScheduler setting learning rate to 0.0005128205.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4751 - acc: 0.8328 - val_loss: 0.5344 - val_acc: 0.8317
    Epoch 36/50
    
    Epoch 00036: LearningRateScheduler setting learning rate to 0.0005.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4681 - acc: 0.8360 - val_loss: 0.5490 - val_acc: 0.8297
    Epoch 37/50
    
    Epoch 00037: LearningRateScheduler setting learning rate to 0.0004878049.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4603 - acc: 0.8406 - val_loss: 0.5436 - val_acc: 0.8321
    Epoch 38/50
    
    Epoch 00038: LearningRateScheduler setting learning rate to 0.0004761905.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4604 - acc: 0.8375 - val_loss: 0.5350 - val_acc: 0.8347
    Epoch 39/50
    
    Epoch 00039: LearningRateScheduler setting learning rate to 0.0004651163.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4610 - acc: 0.8384 - val_loss: 0.5484 - val_acc: 0.8286
    Epoch 40/50
    
    Epoch 00040: LearningRateScheduler setting learning rate to 0.0004545455.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4556 - acc: 0.8412 - val_loss: 0.5717 - val_acc: 0.8236
    Epoch 41/50
    
    Epoch 00041: LearningRateScheduler setting learning rate to 0.0004444444.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4481 - acc: 0.8445 - val_loss: 0.5535 - val_acc: 0.8280
    Epoch 42/50
    
    Epoch 00042: LearningRateScheduler setting learning rate to 0.0004347826.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4509 - acc: 0.8423 - val_loss: 0.5400 - val_acc: 0.8358
    Epoch 43/50
    
    Epoch 00043: LearningRateScheduler setting learning rate to 0.0004255319.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4440 - acc: 0.8440 - val_loss: 0.5296 - val_acc: 0.8363
    Epoch 44/50
    
    Epoch 00044: LearningRateScheduler setting learning rate to 0.0004166667.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4466 - acc: 0.8433 - val_loss: 0.5528 - val_acc: 0.8304
    Epoch 45/50
    
    Epoch 00045: LearningRateScheduler setting learning rate to 0.0004081633.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4487 - acc: 0.8426 - val_loss: 0.5392 - val_acc: 0.8361
    Epoch 46/50
    
    Epoch 00046: LearningRateScheduler setting learning rate to 0.0004.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4434 - acc: 0.8458 - val_loss: 0.5588 - val_acc: 0.8308
    Epoch 47/50
    
    Epoch 00047: LearningRateScheduler setting learning rate to 0.0003921569.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4440 - acc: 0.8441 - val_loss: 0.5167 - val_acc: 0.8407
    Epoch 48/50
    
    Epoch 00048: LearningRateScheduler setting learning rate to 0.0003846154.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4349 - acc: 0.8474 - val_loss: 0.5290 - val_acc: 0.8382
    Epoch 49/50
    
    Epoch 00049: LearningRateScheduler setting learning rate to 0.0003773585.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4369 - acc: 0.8461 - val_loss: 0.5710 - val_acc: 0.8260
    Epoch 50/50
    
    Epoch 00050: LearningRateScheduler setting learning rate to 0.0003703704.
    390/390 [==============================] - 28s 71ms/step - loss: 0.4308 - acc: 0.8497 - val_loss: 0.5876 - val_acc: 0.8269
    Model took 1385.51 seconds to train

