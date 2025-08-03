# CNN_CIFAR-10_auto
Код представляет собой реализацию сверточного автоэнкодера (CNN) на PyTorch для восстановления изображений. Для обучения использовалась часть датасета CIFAR-10 (изображения автомобилей).
результаты выполнения программы:
<img width="637" height="358" alt="image" src="https://github.com/user-attachments/assets/9dd163c6-80bb-4558-9c91-943a44bcbecd" />
<img width="1569" height="319" alt="image" src="https://github.com/user-attachments/assets/74a4b8bf-1d5d-4940-94ac-a31840226285" />
System Information:
  Python Version: 3.11.13
  PyTorch Version: 2.6.0+cu124
  Device: cpu
  Operating System: Linux 6.1.123+
  CPU: x86_64

Model Summary:
  Total parameters: 134691
  Trainable parameters: 134691

  ----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 32, 32, 32]             896
              ReLU-2           [-1, 32, 32, 32]               0
         MaxPool2d-3           [-1, 32, 16, 16]               0
            Conv2d-4           [-1, 64, 16, 16]          18,496
              ReLU-5           [-1, 64, 16, 16]               0
         MaxPool2d-6             [-1, 64, 8, 8]               0
            Conv2d-7            [-1, 128, 8, 8]          73,856
              ReLU-8            [-1, 128, 8, 8]               0
         MaxPool2d-9            [-1, 128, 4, 4]               0
  ConvTranspose2d-10             [-1, 64, 8, 8]          32,832
             ReLU-11             [-1, 64, 8, 8]               0
  ConvTranspose2d-12           [-1, 32, 16, 16]           8,224
             ReLU-13           [-1, 32, 16, 16]               0
  ConvTranspose2d-14            [-1, 3, 32, 32]             387
             Tanh-15            [-1, 3, 32, 32]               0
================================================================
Total params: 134,691
Trainable params: 134,691
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.01
Forward/backward pass size (MB): 1.22
Params size (MB): 0.51
Estimated Total Size (MB): 1.74
----------------------------------------------------------------
