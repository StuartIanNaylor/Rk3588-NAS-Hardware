https://github.com/Tencent/ncnn/tree/master/benchmark

Linux raspberrypi 6.1.0-rpi4-rpi-2712 Rpi5 4GB performance governor
```
pi@raspberrypi:~/ncnn/benchmark $ ../build/benchmark/benchncnn 10 4 0 -1 1
loop_count = 10
num_threads = 4
powersave = 0
gpu_device = -1
cooling_down = 1
          squeezenet  min =    8.04  max =    8.33  avg =    8.19
     squeezenet_int8  min =    7.96  max =    8.27  avg =    8.10
           mobilenet  min =   10.15  max =   10.24  avg =   10.22
      mobilenet_int8  min =   10.13  max =   10.29  avg =   10.18
        mobilenet_v2  min =   11.87  max =   12.05  avg =   11.94
        mobilenet_v3  min =    8.14  max =    8.51  avg =    8.22
          shufflenet  min =    4.22  max =    4.25  avg =    4.23
       shufflenet_v2  min =    3.41  max =    3.49  avg =    3.46
             mnasnet  min =    7.44  max =    7.52  avg =    7.49
     proxylessnasnet  min =    8.44  max =    8.57  avg =    8.51
     efficientnet_b0  min =   13.27  max =   13.45  avg =   13.33
   efficientnetv2_b0  min =   14.94  max =   15.19  avg =   15.06
        regnety_400m  min =   11.32  max =   11.40  avg =   11.36
           blazeface  min =    1.52  max =    1.56  avg =    1.54
           googlenet  min =   27.61  max =   28.16  avg =   27.81
      googlenet_int8  min =   26.40  max =   27.15  avg =   26.70
            resnet18  min =   21.05  max =   21.32  avg =   21.16
       resnet18_int8  min =   18.90  max =   19.24  avg =   19.07
             alexnet  min =   21.61  max =   22.02  avg =   21.87
               vgg16  min =  130.71  max =  132.37  avg =  131.61
          vgg16_int8  min =  109.77  max =  110.40  avg =  110.18
            resnet50  min =   49.50  max =   49.89  avg =   49.69
       resnet50_int8  min =   45.79  max =   46.23  avg =   46.01
      squeezenet_ssd  min =   33.62  max =   34.19  avg =   33.98
 squeezenet_ssd_int8  min =   32.58  max =   33.82  avg =   33.00
       mobilenet_ssd  min =   27.49  max =   27.82  avg =   27.63
  mobilenet_ssd_int8  min =   25.46  max =   26.05  avg =   25.80
      mobilenet_yolo  min =   63.22  max =   63.87  avg =   63.50
  mobilenetv2_yolov3  min =   42.91  max =   43.37  avg =   43.04
         yolov4-tiny  min =   50.24  max =   51.03  avg =   50.57
           nanodet_m  min =   12.89  max =   13.37  avg =   13.19
    yolo-fastest-1.1  min =    5.91  max =    6.00  avg =    5.96
      yolo-fastestv2  min =    5.53  max =    5.63  avg =    5.57
  vision_transformer  min =  581.85  max =  601.10  avg =  592.35
          FastestDet  min =    5.34  max =    5.45  avg =    5.39
pi@raspberrypi:~/ncnn/benchmark $ ../build/benchmark/benchncnn 10 1 0 -1 1
loop_count = 10
num_threads = 1
powersave = 0
gpu_device = -1
cooling_down = 1
          squeezenet  min =   12.52  max =   12.68  avg =   12.61
     squeezenet_int8  min =   12.44  max =   12.82  avg =   12.63
           mobilenet  min =   20.60  max =   20.74  avg =   20.67
      mobilenet_int8  min =   14.75  max =   15.02  avg =   14.90
        mobilenet_v2  min =   17.21  max =   17.55  avg =   17.35
        mobilenet_v3  min =   12.40  max =   12.61  avg =   12.50
          shufflenet  min =    7.19  max =    7.24  avg =    7.21
       shufflenet_v2  min =    7.06  max =    7.18  avg =    7.12
             mnasnet  min =   13.09  max =   13.30  avg =   13.17
     proxylessnasnet  min =   16.01  max =   16.08  avg =   16.04
     efficientnet_b0  min =   24.96  max =   25.07  avg =   25.01
   efficientnetv2_b0  min =   28.38  max =   28.57  avg =   28.48
        regnety_400m  min =   16.71  max =   16.91  avg =   16.81
           blazeface  min =    3.07  max =    3.10  avg =    3.09
           googlenet  min =   49.47  max =   49.90  avg =   49.70
      googlenet_int8  min =   50.45  max =   50.66  avg =   50.53
            resnet18  min =   30.65  max =   31.01  avg =   30.89
       resnet18_int8  min =   37.26  max =   37.49  avg =   37.37
             alexnet  min =   35.60  max =   36.26  avg =   35.85
               vgg16  min =  190.70  max =  192.68  avg =  191.85
          vgg16_int8  min =  273.19  max =  274.39  avg =  273.89
            resnet50  min =   89.31  max =   89.96  avg =   89.63
       resnet50_int8  min =   81.90  max =   82.38  avg =   82.15
      squeezenet_ssd  min =   39.28  max =   39.78  avg =   39.57
 squeezenet_ssd_int8  min =   41.85  max =   42.37  avg =   42.23
       mobilenet_ssd  min =   46.10  max =   47.57  avg =   46.89
  mobilenet_ssd_int8  min =   36.46  max =   37.20  avg =   36.93
      mobilenet_yolo  min =  107.05  max =  109.33  avg =  108.22
  mobilenetv2_yolov3  min =   62.88  max =   63.02  avg =   62.96
         yolov4-tiny  min =   69.93  max =   71.10  avg =   70.53
           nanodet_m  min =   20.51  max =   20.85  avg =   20.70
    yolo-fastest-1.1  min =    8.25  max =    8.42  avg =    8.31
      yolo-fastestv2  min =    7.34  max =    7.46  avg =    7.37
  vision_transformer  min = 1226.23  max = 1228.12  avg = 1227.37
          FastestDet  min =    7.53  max =    7.66  avg =    7.60
```

Linux ubuntu 6.6.0 #1 SMP PREEMPT Opi5 4GB performance governor
```
ubuntu@ubuntu:~/ncnn/benchmark$ ../build/benchmark/benchncnn  10 4 0 -1 1
loop_count = 10
num_threads = 4
powersave = 0
gpu_device = -1
cooling_down = 1
          squeezenet  min =    5.00  max =    5.08  avg =    5.02
     squeezenet_int8  min =    3.96  max =    4.03  avg =    4.00
           mobilenet  min =    8.25  max =    8.29  avg =    8.27
      mobilenet_int8  min =    4.52  max =    4.57  avg =    4.55
        mobilenet_v2  min =    6.18  max =    6.33  avg =    6.24
        mobilenet_v3  min =    5.41  max =    5.43  avg =    5.42
          shufflenet  min =    4.10  max =    4.13  avg =    4.11
       shufflenet_v2  min =    3.62  max =    3.63  avg =    3.63
             mnasnet  min =    5.82  max =    5.84  avg =    5.83
     proxylessnasnet  min =    6.49  max =    6.51  avg =    6.50
     efficientnet_b0  min =    9.56  max =    9.59  avg =    9.58
   efficientnetv2_b0  min =   11.31  max =   11.38  avg =   11.34
        regnety_400m  min =    9.96  max =    9.98  avg =    9.97
           blazeface  min =    1.51  max =    1.59  avg =    1.56
           googlenet  min =   16.90  max =   16.95  avg =   16.92
      googlenet_int8  min =   14.16  max =   14.22  avg =   14.19
            resnet18  min =   11.82  max =   11.89  avg =   11.84
       resnet18_int8  min =   10.43  max =   10.50  avg =   10.48
             alexnet  min =   12.23  max =   12.31  avg =   12.28
               vgg16  min =   77.52  max =   77.77  avg =   77.62
          vgg16_int8  min =   75.63  max =   76.25  avg =   75.87
            resnet50  min =   37.93  max =   38.02  avg =   37.97
       resnet50_int8  min =   23.36  max =   23.40  avg =   23.37
      squeezenet_ssd  min =   14.41  max =   14.54  avg =   14.48
 squeezenet_ssd_int8  min =   12.39  max =   12.86  avg =   12.64
       mobilenet_ssd  min =   18.35  max =   18.57  avg =   18.45
  mobilenet_ssd_int8  min =    9.89  max =    9.97  avg =    9.93
      mobilenet_yolo  min =   44.27  max =   44.42  avg =   44.35
  mobilenetv2_yolov3  min =   24.83  max =   24.91  avg =   24.86
         yolov4-tiny  min =   28.67  max =   28.86  avg =   28.76
           nanodet_m  min =    8.83  max =    8.93  avg =    8.88
    yolo-fastest-1.1  min =    4.63  max =    4.66  avg =    4.64
      yolo-fastestv2  min =    3.77  max =    3.79  avg =    3.77
  vision_transformer  min =  414.35  max =  419.60  avg =  416.31
          FastestDet  min =    3.75  max =    3.77  avg =    3.76
ubuntu@ubuntu:~/ncnn/benchmark$ ../build/benchmark/benchncnn  10 1 0 -1 1
loop_count = 10
num_threads = 1
powersave = 0
gpu_device = -1
cooling_down = 1
          squeezenet  min =   16.05  max =   16.15  avg =   16.10
     squeezenet_int8  min =   10.99  max =   11.06  avg =   11.03
           mobilenet  min =   30.05  max =   30.08  avg =   30.07
      mobilenet_int8  min =   14.83  max =   14.88  avg =   14.85
        mobilenet_v2  min =   18.42  max =   18.49  avg =   18.45
        mobilenet_v3  min =   14.82  max =   14.86  avg =   14.84
          shufflenet  min =    9.52  max =    9.54  avg =    9.53
       shufflenet_v2  min =    9.95  max =    9.98  avg =    9.97
             mnasnet  min =   17.68  max =   17.72  avg =   17.69
     proxylessnasnet  min =   20.81  max =   20.83  avg =   20.81
     efficientnet_b0  min =   30.39  max =   30.42  avg =   30.40
   efficientnetv2_b0  min =   36.39  max =   36.62  avg =   36.52
        regnety_400m  min =   23.02  max =   23.07  avg =   23.03
           blazeface  min =    3.51  max =    3.52  avg =    3.52
           googlenet  min =   54.90  max =   55.03  avg =   54.97
      googlenet_int8  min =   43.19  max =   43.24  avg =   43.21
            resnet18  min =   37.57  max =   37.68  avg =   37.62
       resnet18_int8  min =   35.11  max =   35.29  avg =   35.19
             alexnet  min =   33.69  max =   33.78  avg =   33.73
               vgg16  min =  238.96  max =  240.73  avg =  239.75
          vgg16_int8  min =  280.12  max =  281.07  avg =  280.53
            resnet50  min =  132.17  max =  132.66  avg =  132.40
       resnet50_int8  min =   75.62  max =   75.71  avg =   75.66
      squeezenet_ssd  min =   37.79  max =   37.87  avg =   37.84
 squeezenet_ssd_int8  min =   32.36  max =   32.44  avg =   32.39
       mobilenet_ssd  min =   62.82  max =   62.95  avg =   62.88
  mobilenet_ssd_int8  min =   30.90  max =   30.98  avg =   30.93
      mobilenet_yolo  min =  143.75  max =  143.99  avg =  143.87
  mobilenetv2_yolov3  min =   70.35  max =   70.41  avg =   70.37
         yolov4-tiny  min =   80.23  max =   80.89  avg =   80.55
           nanodet_m  min =   24.42  max =   24.48  avg =   24.45
    yolo-fastest-1.1  min =    9.16  max =    9.19  avg =    9.18
      yolo-fastestv2  min =    7.98  max =    8.02  avg =    7.99
  vision_transformer  min = 1192.51  max = 1193.71  avg = 1193.03
          FastestDet  min =    8.38  max =    8.41  avg =    8.40
```
