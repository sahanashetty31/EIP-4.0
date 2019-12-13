### Final Validation accuracy for Base Network ###
82.47

### Final validation accuracy of my network ###
83.27

### Model definition with output channel size and receptive field ###
# Define the model
model2 = Sequential()


model2.add(SeparableConv2D(64, kernel_size=(3, 3), activation='relu', input_shape=(32, 32, 3), padding='same')) #O/P channel size - 32x32x64, RF=3
model2.add(BatchNormalization())

model2.add(SeparableConv2D(64, kernel_size=(3, 3), activation='relu'))#O/P channel size - 30x30x64, RF=5
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu', padding='same'))#O/P channel size - 30x30x128, RF=7
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(MaxPooling2D(pool_size=(2, 2))) #O/P channel size - 15x15x128, RF=8

model2.add(Convolution2D(64, 1, 1 , activation='relu')) #O/P channel size - 15x15x64, RF=8
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(SeparableConv2D(96, kernel_size=(3, 3), activation='relu',padding='same')) # O/P channel size - 15x15x96, RF=12
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu')) #O/P channel size - 13x13x128, RF=16
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(MaxPooling2D(pool_size=(2, 2))) #O/P channel size - 6x6x128,RF=18

model2.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu')) #O/P channel size - 4x4x128, RF=26
model2.add(BatchNormalization())
model2.add(Dropout(0.1))

model2.add(SeparableConv2D(10, kernel_size=(3, 3), activation='relu')) #O/P channel size - 2x2x10, RF=34
model2.add(BatchNormalization())

model2.add(GlobalAveragePooling2D()) #O/P channel size - 1x1x10
model2.add(Activation('softmax'))

model2.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

### 50 epoch logs ###

Epoch 1/50
390/390 [==============================] - 21s 55ms/step - loss: 1.4568 - acc: 0.5029 - val_loss: 1.1427 - val_acc: 0.6077
Epoch 2/50
390/390 [==============================] - 19s 50ms/step - loss: 1.0396 - acc: 0.6609 - val_loss: 1.0085 - val_acc: 0.6591
Epoch 3/50
390/390 [==============================] - 19s 50ms/step - loss: 0.8750 - acc: 0.7145 - val_loss: 0.8485 - val_acc: 0.7171
Epoch 4/50
390/390 [==============================] - 19s 50ms/step - loss: 0.7755 - acc: 0.7446 - val_loss: 0.7899 - val_acc: 0.7335
Epoch 5/50
390/390 [==============================] - 19s 50ms/step - loss: 0.7040 - acc: 0.7667 - val_loss: 0.7205 - val_acc: 0.7555
Epoch 6/50
390/390 [==============================] - 19s 50ms/step - loss: 0.6494 - acc: 0.7844 - val_loss: 0.7028 - val_acc: 0.7624
Epoch 7/50
390/390 [==============================] - 19s 50ms/step - loss: 0.6127 - acc: 0.7970 - val_loss: 0.6379 - val_acc: 0.7837
Epoch 8/50
390/390 [==============================] - 19s 50ms/step - loss: 0.5759 - acc: 0.8061 - val_loss: 0.6766 - val_acc: 0.7738
Epoch 9/50
390/390 [==============================] - 19s 50ms/step - loss: 0.5479 - acc: 0.8156 - val_loss: 0.6037 - val_acc: 0.7963
Epoch 10/50
390/390 [==============================] - 19s 50ms/step - loss: 0.5207 - acc: 0.8256 - val_loss: 0.6067 - val_acc: 0.7987
Epoch 11/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4992 - acc: 0.8330 - val_loss: 0.6439 - val_acc: 0.7820
Epoch 12/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4770 - acc: 0.8381 - val_loss: 0.6216 - val_acc: 0.7878
Epoch 13/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4589 - acc: 0.8460 - val_loss: 0.5723 - val_acc: 0.8079
Epoch 14/50
390/390 [==============================] - 20s 50ms/step - loss: 0.4435 - acc: 0.8496 - val_loss: 0.6016 - val_acc: 0.8027
Epoch 15/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4309 - acc: 0.8551 - val_loss: 0.6214 - val_acc: 0.7985
Epoch 16/50
390/390 [==============================] - 19s 50ms/step - loss: 0.4163 - acc: 0.8593 - val_loss: 0.5981 - val_acc: 0.8055
Epoch 17/50
390/390 [==============================] - 19s 49ms/step - loss: 0.4051 - acc: 0.8627 - val_loss: 0.5959 - val_acc: 0.8072
Epoch 18/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3961 - acc: 0.8645 - val_loss: 0.5683 - val_acc: 0.8132
Epoch 19/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3823 - acc: 0.8685 - val_loss: 0.6057 - val_acc: 0.7973
Epoch 20/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3708 - acc: 0.8722 - val_loss: 0.5675 - val_acc: 0.8134
Epoch 21/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3620 - acc: 0.8747 - val_loss: 0.5814 - val_acc: 0.8110
Epoch 22/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3525 - acc: 0.8781 - val_loss: 0.5818 - val_acc: 0.8137
Epoch 23/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3487 - acc: 0.8805 - val_loss: 0.5826 - val_acc: 0.8140
Epoch 24/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3349 - acc: 0.8864 - val_loss: 0.5689 - val_acc: 0.8156
Epoch 25/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3317 - acc: 0.8865 - val_loss: 0.5613 - val_acc: 0.8143
Epoch 26/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3288 - acc: 0.8869 - val_loss: 0.5853 - val_acc: 0.8147
Epoch 27/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3183 - acc: 0.8900 - val_loss: 0.5488 - val_acc: 0.8261
Epoch 28/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3107 - acc: 0.8927 - val_loss: 0.5812 - val_acc: 0.8167
Epoch 29/50
390/390 [==============================] - 19s 50ms/step - loss: 0.3060 - acc: 0.8944 - val_loss: 0.5941 - val_acc: 0.8089
Epoch 30/50
390/390 [==============================] - 20s 50ms/step - loss: 0.2977 - acc: 0.8973 - val_loss: 0.5628 - val_acc: 0.8302
Epoch 31/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2939 - acc: 0.8977 - val_loss: 0.5773 - val_acc: 0.8233
Epoch 32/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2916 - acc: 0.8977 - val_loss: 0.5600 - val_acc: 0.8226
Epoch 33/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2849 - acc: 0.9014 - val_loss: 0.5974 - val_acc: 0.8153
Epoch 34/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2768 - acc: 0.9045 - val_loss: 0.5790 - val_acc: 0.8199
Epoch 35/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2770 - acc: 0.9042 - val_loss: 0.5713 - val_acc: 0.8228
Epoch 36/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2706 - acc: 0.9045 - val_loss: 0.5602 - val_acc: 0.8266
Epoch 37/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2657 - acc: 0.9064 - val_loss: 0.5763 - val_acc: 0.8207
Epoch 38/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2660 - acc: 0.9073 - val_loss: 0.5777 - val_acc: 0.8234
Epoch 39/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2652 - acc: 0.9074 - val_loss: 0.5470 - val_acc: 0.8270
Epoch 40/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2573 - acc: 0.9090 - val_loss: 0.5856 - val_acc: 0.8241
Epoch 41/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2553 - acc: 0.9112 - val_loss: 0.5701 - val_acc: 0.8259
Epoch 42/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2523 - acc: 0.9112 - val_loss: 0.5620 - val_acc: 0.8274
Epoch 43/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2473 - acc: 0.9127 - val_loss: 0.5646 - val_acc: 0.8278
Epoch 44/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2451 - acc: 0.9154 - val_loss: 0.5958 - val_acc: 0.8259
Epoch 45/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2418 - acc: 0.9144 - val_loss: 0.5640 - val_acc: 0.8281
Epoch 46/50
390/390 [==============================] - 20s 50ms/step - loss: 0.2357 - acc: 0.9169 - val_loss: 0.5718 - val_acc: 0.8275
Epoch 47/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2362 - acc: 0.9173 - val_loss: 0.6081 - val_acc: 0.8185
Epoch 48/50
390/390 [==============================] - 19s 49ms/step - loss: 0.2337 - acc: 0.9190 - val_loss: 0.5842 - val_acc: 0.8253
Epoch 49/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2250 - acc: 0.9207 - val_loss: 0.6032 - val_acc: 0.8245
Epoch 50/50
390/390 [==============================] - 19s 50ms/step - loss: 0.2304 - acc: 0.9204 - val_loss: 0.5644 - val_acc: 0.8327
Model took 974.62 seconds to train

Accuracy on test data is: 83.27
