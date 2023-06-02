### default
```python
x = Convolution2D(24, (5,5), strides=(2,2), activation='relu', name="conv2d_1")(x)
x = Dropout(drop)(x)
x = Convolution2D(32, (5,5), strides=(2,2), activation='relu', name="conv2d_2")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (5,5), strides=(2,2), activation='relu', name="conv2d_3")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (3,3), strides=(1,1), activation='relu', name="conv2d_4")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (3,3), strides=(1,1), activation='relu', name="conv2d_5")(x)
x = Dropout(drop)(x)
x = Flatten(name='flattened')(x)
x = Dense(100, activation='relu')(x)
x = Dropout(drop)(x)
x = Dense(50, activation='relu')(x)
x = Dropout(drop)(x)
```
loss: 0.0801
n_outputs0_loss: 0.0774
n_outputs1_loss: 0.0027
val_loss: 0.1388
val_n_outputs0_loss: 0.1364
val_n_outputs1_loss: 0.0023
![img.png](img.png)

### dense1
```python
x = Convolution2D(24, (5,5), strides=(2,2), activation='relu', name="conv2d_1")(x)
x = Dropout(drop)(x)
x = Convolution2D(32, (5,5), strides=(2,2), activation='relu', name="conv2d_2")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (5,5), strides=(2,2), activation='relu', name="conv2d_3")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (3,3), strides=(1,1), activation='relu', name="conv2d_4")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (3,3), strides=(1,1), activation='relu', name="conv2d_5")(x)
x = Dropout(drop)(x)
x = Flatten(name='flattened')(x)
x = Dense(100, activation='relu')(x)
x = Dropout(drop)(x)
x = Dense(100, activation='relu')(x)
x = Dropout(drop)(x)
x = Dense(50, activation='relu')(x)
x = Dropout(drop)(x)
```
loss: 0.0456
n_outputs0_loss: 0.0432
n_outputs1_loss: 0.0024 - val_loss: 0.1388 
val_n_outputs0_loss: 0.1369 
val_n_outputs1_loss: 0.0019

![img_1.png](img_1.png)

### conv128ch
```python
x = img_in
x = Convolution2D(24, (5,5), strides=(2,2), activation='relu', name="conv2d_1")(x)
x = Dropout(drop)(x)
x = Convolution2D(32, (5,5), strides=(2,2), activation='relu', name="conv2d_2")(x)
x = Dropout(drop)(x)
x = Convolution2D(64, (5,5), strides=(2,2), activation='relu', name="conv2d_3")(x)
x = Dropout(drop)(x)
x = Convolution2D(128, (3,3), strides=(1,1), activation='relu', name="conv2d_4")(x)
x = Dropout(drop)(x)
x = Convolution2D(128, (3,3), strides=(1,1), activation='relu', name="conv2d_5")(x)
x = Dropout(drop)(x)
x = Flatten(name='flattened')(x)
x = Dense(100, activation='relu')(x)
x = Dropout(drop)(x)
x = Dense(50, activation='relu')(x)
x = Dropout(drop)(x)
```
