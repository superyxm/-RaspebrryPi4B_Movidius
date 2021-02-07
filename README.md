# RaspebrryPi4B_Movidius

This project aims to make RaspberryPi 4B works with Intel Nerual Compute Stick Movidius.

Device:

![image](https://github.com/superyxm/RaspebrryPi4B_Movidius/blob/main/mydevice.jpg)

RaspberryPi 4B 4GB(I used 4GB version, I think 2GB version is also OK. 8GB version is better.)
Intel Nerual Compute Stick Movidius (I used Nerual Compute Stick 1, not the second generation just because it is much cheaper)

Enviroment:

1.Intel said Nerual Compute Stick 1 (Intel NCS1) will not be supported. I have tried some Openvino version, and I find I can success on version 2020.1.023 while I faild in newer version. Download openvinotoolkit from
  https://download.01.org/opencv/2020/openvinotoolkit/2020.1/l_openvino_toolkit_runtime_raspbian_p_2020.1.023.tgz

2.Follow the following website to install openvinotoolkit. Note new version model file didn't work. See next guide.
  https://docs.openvinotoolkit.org/cn/latest/openvino_docs_install_guides_installing_openvino_raspbian.html#install-package
  
3.I haved test and found that only some version such as version 2019 models are compatible with Intel NCS1. So I recommand to use these models from
  https://download.01.org/opencv/2019/open_model_zoo/R1/models_bin/
  
Note:
1.You can overclock your RaspebrryPi 4B CPU to 2.0GHz by adding following configuration to  /boot/config.txt:

  force_turbo=0
  
  arm_freq=2000
  
  over_voltage=6
  
  
Reference:
1. https://zhuanlan.zhihu.com/p/64012705 (In this article, It help me build simple opencv demo quickly.)
2. https://www.rs-online.com/designspark/raspberry-pi-4intel-1-cn (I found version 2019 models are compatible with Intel NCS1.)
3. https://docs.openvinotoolkit.org/cn/latest/openvino_docs_install_guides_installing_openvino_raspbian.html
4. https://segmentfault.com/a/1190000037440525
5. https://zhuanlan.zhihu.com/p/76437760
