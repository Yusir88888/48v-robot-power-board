<div align="center">

# 48V 基于LM5148 多路输出机器人运控电源板





> 基于48V锂电池架构一体化供电板卡，集成多路DC-DC电源 + CAN总线通信，用于机器人48V关节模组运动控制系统供电和通信

</div>

## 📖 项目简介
本项目为机器人电控专用电源板卡，采用德州仪器 **LM5148** DC-DC电源芯片，通过XT60端子接入48V锂电池输入。
板卡实现多路稳压电源输出：**5V、12V、16V**，同时集成CAN总线与RJ45网口。
网口支持对接EtherCAT从站设备以及X86主控平台，实现机器人供电与运动控制通信一体化，减少电控柜内模块数量，简化机器人电控布局。
项目开源包含完整Altium Designer原理图、PCB工程、BOM物料清单，可直接打板、二次修改开发。

## ✨ 核心功能
- 🔋 输入接口：XT60，适配48V锂电池包
- ⚡ 多路电源输出：5V / 12V / 16V，为伺服、传感器、主控供电
- 📡 CAN总线：板载CAN通信接口，用于设备间低速总线交互
- 🌐 RJ45网口：支持EtherCAT从站通信，对接X86运动控制主机
- 🤖 适用场景：协作机器人、移动机器人、关节模组运动控制系统

## 🛠️ 技术方案 & 设计要点
- 主控电源芯片：TI TPS5148
- 设计软件：Altium Designer
- 供电架构：48V转多路低压DC-DC降压
- 通信协议：CAN 2.0B、EtherCAT
- 板卡类型：电源+通信一体化集成板

> 💡 设计难点：
> 高压48V电源轨与EtherCAT高速信号、CAN信号同板布局，在布线时做好功率区域与信号区域分区，处理地平面分割、回流路径，降低开关电源对高速总线的电磁干扰，保证运动控制通信稳定。

## 🖼️ 工程预览
<img width="807" height="635" alt="e21ab2f6e993d53a88b854bfc06bc4e9" src="https://github.com/user-attachments/assets/6ca45167-83cc-46c6-af19-ab00ade7d50f" />
<img width="1702" height="1276" alt="cffa8cc3a884bab252c912dc23907876" src="https://github.com/user-attachments/assets/a5e8fe92-bc9f-4d5c-982b-85247fcf4730" />
