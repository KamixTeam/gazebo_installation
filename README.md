# Gazebo Kurulumu

Bu rehber, Ubuntu işletim sistemi üzerinde Python, ArduPilot, MAVProxy, Gazebo, ve diğer gerekli yazılımları kurmak için kullanabileceğiniz adımları içerir. Aşağıdaki adımları takip ederek simülasyon dünyasını başlatabilirsiniz.

## Python Kurulumu

Python'ı yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [Python Kurulum Kılavuzu](https://phoenixnap.com/kb/how-to-install-python-3-ubuntu).

## PIP Kurulumu

PIP'i yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [PIP Kurulum Kılavuzu](https://phoenixnap.com/kb/how-to-install-pip-on-ubuntu).

## ArduPilot ve MAVProxy Kurulumu

ArduPilot ve MAVProxy'yi yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [ArduPilot ve MAVProxy Kurulum Kılavuzu](https://github.com/Intelligent-Quads/iq_tutorials/blob/master/docs/Installing_Ardupilot.md).

- Eğer "mavgen returned 1 error code" hatası alıyorsanız, `pip install future` komutu ile gerekli bağımlılığı yükleyin ve kurulumu tekrar deneyin.

- "Defaulting to user installation because normal site-packages is not writeable" hatası alıyorsanız, `sudo python -m pip install --upgrade pip` komutunu kullanarak sorunu çözebilirsiniz.

## QGroundControl Kurulumu

QGroundControl'ü yüklemek için aşağıdaki adımları izleyin:

1. `sudo apt install libsdl2-dev` komutu ile gerekli bağımlılığı kurun.

2. [QGroundControl Dosyasını İndirin](https://github.com/Intelligent-Quads/iq_tutorials/blob/master/docs/installing_qgc.md).

## Gazebo ve ArduPilot Eklentisinin Kurulumu

Gazebo ve ArduPilot eklentisini yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [Gazebo ve ArduPilot Eklentisi Kurulum Kılavuzu](https://github.com/Intelligent-Quads/iq_tutorials/blob/master/docs/installing_gazebo_arduplugin.md).

- Eğer "Gazebo Invalid Argument Hatası" alıyorsanız, `export SVGA_VGPU10=0` komutunu çalıştırarak sorunu giderebilirsiniz.

## MAVProxy Kurulumu

MAVProxy'yi yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [MAVProxy Kurulum Kılavuzu](https://ardupilot.org/mavproxy/docs/getting_started/download_and_installation.html#linux).

## PyMAVLINK Yükleme

PyMAVLINK'i yüklemek için `pip install pymavlink` komutunu kullanabilirsiniz.

## DroneKit Kurulumu

DroneKit'i yüklemek için aşağıdaki adımları izleyin:

1. DroneKit Python kütüphanesini [resmi belgelendirmeden](https://dronekit-python.readthedocs.io/en/latest/develop/installation.html) yükleyin.

## OpenCV Kurulumu

OpenCV'yi yüklemek için aşağıdaki kaynağı kullanabilirsiniz: [OpenCV Kurulum Kılavuzu](https://linuxize.com/post/how-to-install-opencv-on-ubuntu-18-04).

## Simülasyonu Başlatma

- Gazebo simülasyon dünyasını başlatmak için aşağıdaki komutu kullanabilirsiniz:
  `gazebo --verbose worlds/iris_arducopter_runway.world`
- ArduPilot'u simülasyon modunda çalıştırmak için aşağıdaki komutları kullanabilirsiniz:
```
cd ~/ardupilot/ArduCopter
../Tools/autotest/sim_vehicle.py -f gazebo-iris --console --map
```

Simülasyon dünyasını ve ilgili yazılımları bu adımları takip ederek başarılı bir şekilde kurabilirsiniz.


