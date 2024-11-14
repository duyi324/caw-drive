# 🐦 CawDrive - 无刷电机驱动器

---

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/H2H3PQZVW)

# 🚀 简介

- 支持 24 电压输入

- 当前版本支持 SPI，串口和 CAN FD 总线通讯,支持 TIM PWM 刹车功能

- 主控芯片：STM32G474，电机驱动芯片为 DRV8323RSRGZR

- 板载磁编码器：AS5047P

- 支持一路NTC采样

- 支持 6xPWM 和 3xPWM 的控制

# 🗂️ 目录

* Firmware：FOC控制的实际控制代码以及STM32CubeMX配置

* PCB：FOC驱动器原理图、PCB以及生成的Gerber文件

# 📦 固件编译

## 配置caw-embedded库

当前固件编译依赖caw-embedded项目: https://github.com/fake-rick/caw-embedded

依赖添加方式1：

可以直接将caw-embedded项目克隆到caw-drive/Firmware目录下:

```bash
cd caw-drive/Firmware
git clone git@github.com:fake-rick/caw-embedded.git caw_embedded
```

依赖添加方式2：

将caw-embedded项目克隆后建立链接（Linux），假设将caw-embedded放在与caw-drive同级目录下:

```bash
git clone git@github.com:fake-rick/caw-embedded.git
cd caw-drive/Firmware
ln -s ../../caw-embedded caw_embedded
```

## VSCode配置

安装并配置stm32-for-vscode插件

# 🖥️ 上位机

![](https://github.com/fake-rick/caw-drive/blob/master/Docs/imgs/cawstudio.png)

# 📝 参考资料

https://github.com/bgkatz/3phase_integrated

https://github.com/simplefoc/Arduino-FOC
