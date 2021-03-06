# CarDetection-Keras
"Car Detection" is trained in Keras using Tensorflow as back-end. It's taking an image as input and it  
gives a binary decision whether a car is present in the image or not. It's a Dense Neural Network. After train, converting the .h5 model
into .mlmodel to use in Xcode. (Please check the CarDetection-iOS project for that :  https://github.com/ashislaha/CarDetection-iOS ).

Training Data set is uploaded in https://drive.google.com/drive/folders/0B0QC-w3ZqaT1RzlGeGtYeVE2cTA   OR 
https://s3.ap-south-1.amazonaws.com/car-detection-images/Archive.zip .

Put the data set into your working 
directory to train the model. It contains around 1500 training data & 100 test data where both car & non-car images are present.

If you want to test a random image whether car is present in the image or not : 
goto "model" directory -->  paste your image in "test" folder --> $ python predictions.py --file='test/your_image'

Used both Convolutional Neural Network(CNN) & Dense Neural Network(DNN) to train the model. 

CNN gives 99.6% accuracy on Training data & 88.6% on Test data.
DNN gives 92%   accuracy on Training data & 87% on Test data.

Used Metrics to train in CNN : loss='binary_crossentropy', metrics=['accuracy'], optimizer='adadelta'

Used Metrics to train in DNN : loss='binary_crossentropy', metrics=['accuracy'], optimizer='rmsprop'

CNN TRAIN RESULTS : 

1475/1475 [==============================] - 14s - loss: 0.6336 - acc: 0.6142 - val_loss: 0.6956 - val_acc: 0.9207

Epoch 2/25
1475/1475 [==============================] - 15s - loss: 0.5122 - acc: 0.7620 - val_loss: 0.8328 - val_acc: 0.6524

Epoch 3/25
1475/1475 [==============================] - 16s - loss: 0.4236 - acc: 0.8210 - val_loss: 0.2083 - val_acc: 0.9573

Epoch 4/25
1475/1475 [==============================] - 16s - loss: 0.3493 - acc: 0.8508 - val_loss: 0.4898 - val_acc: 0.8537

Epoch 5/25
1475/1475 [==============================] - 16s - loss: 0.2797 - acc: 0.8942 - val_loss: 0.5409 - val_acc: 0.8171

Epoch 6/25
1475/1475 [==============================] - 15s - loss: 0.2392 - acc: 0.9119 - val_loss: 0.5585 - val_acc: 0.8049

Epoch 7/25
1475/1475 [==============================] - 15s - loss: 0.2006 - acc: 0.9281 - val_loss: 0.5729 - val_acc: 0.7683

Epoch 8/25
1475/1475 [==============================] - 15s - loss: 0.1705 - acc: 0.9403 - val_loss: 0.3006 - val_acc: 0.9146

Epoch 9/25
1475/1475 [==============================] - 15s - loss: 0.1404 - acc: 0.9539 - val_loss: 0.0538 - val_acc: 0.9878

Epoch 10/25
1475/1475 [==============================] - 15s - loss: 0.1152 - acc: 0.9647 - val_loss: 0.2950 - val_acc: 0.9085

Epoch 11/25
1475/1475 [==============================] - 15s - loss: 0.0961 - acc: 0.9776 - val_loss: 0.2111 - val_acc: 0.9329

Epoch 12/25
1475/1475 [==============================] - 15s - loss: 0.0770 - acc: 0.9817 - val_loss: 0.3777 - val_acc: 0.8841

Epoch 13/25
1475/1475 [==============================] - 15s - loss: 0.0631 - acc: 0.9864 - val_loss: 0.2729 - val_acc: 0.9329

Epoch 14/25
1475/1475 [==============================] - 15s - loss: 0.0503 - acc: 0.9905 - val_loss: 0.4031 - val_acc: 0.8963

Epoch 15/25
1475/1475 [==============================] - 17s - loss: 0.0440 - acc: 0.9905 - val_loss: 0.3678 - val_acc: 0.8963

Epoch 16/25
1475/1475 [==============================] - 17s - loss: 0.0320 - acc: 0.9946 - val_loss: 0.1558 - val_acc: 0.9512

Epoch 17/25
1475/1475 [==============================] - 17s - loss: 0.0285 - acc: 0.9932 - val_loss: 0.3010 - val_acc: 0.9329

Epoch 18/25
1475/1475 [==============================] - 20s - loss: 0.0245 - acc: 0.9953 - val_loss: 0.3219 - val_acc: 0.9268

Epoch 19/25
1475/1475 [==============================] - 22s - loss: 0.0214 - acc: 0.9966 - val_loss: 0.4263 - val_acc: 0.9085

Epoch 20/25
1475/1475 [==============================] - 21s - loss: 0.0172 - acc: 0.9973 - val_loss: 0.4255 - val_acc: 0.9024

Epoch 21/25
1475/1475 [==============================] - 19s - loss: 0.0155 - acc: 0.9959 - val_loss: 0.2827 - val_acc: 0.9390

Epoch 22/25
1475/1475 [==============================] - 18s - loss: 0.0146 - acc: 0.9959 - val_loss: 0.3245 - val_acc: 0.9329

Epoch 23/25
1475/1475 [==============================] - 18s - loss: 0.0158 - acc: 0.9959 - val_loss: 0.2655 - val_acc: 0.9390

Epoch 24/25
1475/1475 [==============================] - 17s - loss: 0.0116 - acc: 0.9966 - val_loss: 0.3174 - val_acc: 0.9329

Epoch 25/25
1475/1475 [==============================] - 16s - loss: 0.0104 - acc: 0.9966 - val_loss: 0.3039 - val_acc: 0.9329

238/238 [==============================] - 0s     
('\nTest accuracy:', 0.8865546223496189)



DNN TRAIN RESULTS : 

This is the accuray after trained by 50 epochs , almost 92% accurate on train data & on unknown test data 87% accurate

1639/1639 [==============================] - 1s - loss: 5.9528 - acc: 0.4997      
Epoch 2/50
1639/1639 [==============================] - 1s - loss: 0.7847 - acc: 0.6516     
Epoch 3/50
1639/1639 [==============================] - 1s - loss: 0.6361 - acc: 0.6840     
Epoch 4/50
1639/1639 [==============================] - 1s - loss: 0.6202 - acc: 0.6901     
Epoch 5/50
1639/1639 [==============================] - 1s - loss: 0.5706 - acc: 0.7035     
Epoch 6/50
1639/1639 [==============================] - 1s - loss: 0.5586 - acc: 0.7212     
Epoch 7/50
1639/1639 [==============================] - 1s - loss: 0.5272 - acc: 0.7364     
Epoch 8/50
1639/1639 [==============================] - 1s - loss: 0.5192 - acc: 0.7572     
Epoch 9/50
1639/1639 [==============================] - 1s - loss: 0.4962 - acc: 0.7608     
Epoch 10/50
1639/1639 [==============================] - 1s - loss: 0.4754 - acc: 0.7749     
Epoch 11/50
1639/1639 [==============================] - 1s - loss: 0.4548 - acc: 0.7877     
Epoch 12/50
1639/1639 [==============================] - 1s - loss: 0.4559 - acc: 0.7993     
Epoch 13/50
1639/1639 [==============================] - 1s - loss: 0.4350 - acc: 0.7999     
Epoch 14/50
1639/1639 [==============================] - 1s - loss: 0.4194 - acc: 0.8212     
Epoch 15/50
1639/1639 [==============================] - 1s - loss: 0.3927 - acc: 0.8170     
Epoch 16/50
1639/1639 [==============================] - 1s - loss: 0.3953 - acc: 0.8231     
Epoch 17/50
1639/1639 [==============================] - 1s - loss: 0.3828 - acc: 0.8286     
Epoch 18/50
1639/1639 [==============================] - 1s - loss: 0.3720 - acc: 0.8383     
Epoch 19/50
1639/1639 [==============================] - 1s - loss: 0.3543 - acc: 0.8408     
Epoch 20/50
1639/1639 [==============================] - 1s - loss: 0.3486 - acc: 0.8475     
Epoch 21/50
1639/1639 [==============================] - 1s - loss: 0.3400 - acc: 0.8481     
Epoch 22/50
1639/1639 [==============================] - 1s - loss: 0.3153 - acc: 0.8542     
Epoch 23/50
1639/1639 [==============================] - 1s - loss: 0.3149 - acc: 0.8633     
Epoch 24/50
1639/1639 [==============================] - 1s - loss: 0.2994 - acc: 0.8700     
Epoch 25/50
1639/1639 [==============================] - 1s - loss: 0.2977 - acc: 0.8658     
Epoch 26/50
1639/1639 [==============================] - 1s - loss: 0.2908 - acc: 0.8713     
Epoch 27/50
1639/1639 [==============================] - 1s - loss: 0.2725 - acc: 0.8761     
Epoch 28/50
1639/1639 [==============================] - 1s - loss: 0.2640 - acc: 0.8914     
Epoch 29/50
1639/1639 [==============================] - 1s - loss: 0.2467 - acc: 0.8883     
Epoch 30/50
1639/1639 [==============================] - 1s - loss: 0.2375 - acc: 0.8932     
Epoch 31/50
1639/1639 [==============================] - 1s - loss: 0.2549 - acc: 0.8883     
Epoch 32/50
1639/1639 [==============================] - 1s - loss: 0.2557 - acc: 0.8926     
Epoch 33/50
1639/1639 [==============================] - 1s - loss: 0.2406 - acc: 0.8993     
Epoch 34/50
1639/1639 [==============================] - 1s - loss: 0.2407 - acc: 0.8981     
Epoch 35/50
1639/1639 [==============================] - 1s - loss: 0.2246 - acc: 0.9024     
Epoch 36/50
1639/1639 [==============================] - 1s - loss: 0.2290 - acc: 0.9091     
Epoch 37/50
1639/1639 [==============================] - 1s - loss: 0.2134 - acc: 0.9109     
Epoch 38/50
1639/1639 [==============================] - 1s - loss: 0.2129 - acc: 0.9048     
Epoch 39/50
1639/1639 [==============================] - 1s - loss: 0.2411 - acc: 0.9073     
Epoch 40/50
1639/1639 [==============================] - 1s - loss: 0.1841 - acc: 0.9158     
Epoch 41/50
1639/1639 [==============================] - 1s - loss: 0.2019 - acc: 0.9182     
Epoch 42/50
1639/1639 [==============================] - 1s - loss: 0.1755 - acc: 0.9207     
Epoch 43/50
1639/1639 [==============================] - 1s - loss: 0.2057 - acc: 0.9140     
Epoch 44/50
1639/1639 [==============================] - 1s - loss: 0.1791 - acc: 0.9219     
Epoch 45/50
1639/1639 [==============================] - 1s - loss: 0.1613 - acc: 0.9256     
Epoch 46/50
1639/1639 [==============================] - 1s - loss: 0.1857 - acc: 0.9176     
Epoch 47/50
1639/1639 [==============================] - 1s - loss: 0.1731 - acc: 0.9182     
Epoch 48/50
1639/1639 [==============================] - 1s - loss: 0.1661 - acc: 0.9286     
Epoch 49/50
1639/1639 [==============================] - 1s - loss: 0.1607 - acc: 0.9213     
Epoch 50/50
1639/1639 [==============================] - 1s - loss: 0.1721 - acc: 0.9201     
 32/238 [===>..........................] - ETA: 0s('\nTest accuracy:', 0.87394957832929465)
