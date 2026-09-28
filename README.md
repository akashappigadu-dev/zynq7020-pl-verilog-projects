# Zynq-7020 PL 端 Verilog 学习项目

这是一套为 **50MHz Zynq-7020 开发板** 设计的 **PL（FPGA 可编程逻辑）端** 的完整 Verilog 学习项目集合。

## 📋 项目特点

- ✅ **从入门到进阶** - 从 LED 闪烁到 LCD 显示的完整进阶路线
- ✅ **即插即用** - 包含所有 XDC 约束文件和项目配置
- ✅ **详细注释** - 每个 Verilog 模块都有中文注释和讲解
- ✅ **完整测试** - 提供仿真文件（testbench）
- ✅ **Vivado 工程** - 可直接在 Vivado 中打开

## 🎯 学习路线

### 第一阶段：基础数字逻辑（第 1-5 周）

| 项目 | 难度 | 文件位置 | 学习内容 |
|------|------|--------|--------|
| 1. LED 闪烁 | ⭐ | `01_led_blink/` | 时钟分频、计数器、输出 |
| 2. 按键控制 LED | ⭐⭐ | `02_button_led/` | 输入同步、消抖、组合逻辑 |
| 3. 按键计数器 | ⭐⭐ | `03_key_counter/` | 上升沿检测、计数 |
| 4. 7 段数码管 | ⭐⭐⭐ | `04_seg_display/` | 动态扫描、编码/译码 |
| 5. 交通灯控制 | ⭐⭐⭐ | `05_traffic_light/` | FSM（有限状态机）、定时控制 |

### 第二阶段：时序与接口（第 6-10 周）

| 项目 | 难度 | 文件位置 | 学习内容 |
|------|------|--------|--------|
| 6. PWM 呼吸灯 | ⭐⭐ | `06_pwm_breathing/` | PWM、占空比控制 |
| 7. UART 接收器 | ⭐⭐⭐ | `07_uart_rx/` | 串口通信、波特率、数据帧 |
| 8. UART 收发器 | ⭐⭐⭐⭐ | `08_uart_txrx/` | 完整收发、FIFO、流控 |
| 9. 蜂鸣器（PWM） | ⭐⭐ | `09_beeper/` | 音频频率生成 |
| 10. 触摸按键检测 | ⭐⭐⭐ | `10_touch_key/` | 触摸感应处理 |

### 第三阶段：高级项目（第 11-15 周）

| 项目 | 难度 | 文件位置 | 学习内容 |
|------|------|--------|--------|
| 11. VGA 显示 | ⭐⭐⭐⭐ | `11_vga_display/` | VGA 时序、像素输出、颜色 |
| 12. LCD 显示屏 | ⭐⭐⭐⭐⭐ | `12_lcd_display/` | RGB LCD 时序、帧缓存、DMA |
| 13. HDMI 输出 | ⭐⭐⭐⭐⭐ | `13_hdmi_output/` | HDMI 差分信号、TMDS 编码 |
| 14. 摄像头采集 | ⭐⭐⭐⭐⭐ | `14_camera_capture/` | OV5640/OV7725、SCCB、图像处理 |
| 15. 图像边缘检测 | ⭐⭐⭐⭐⭐ | `15_image_sobel/` | Sobel 算子、卷积、实时处理 |

## 📁 仓库结构

```
zynq7020-pl-verilog-projects/
├── README.md                          # 本文件
├── docs/                              # 文档和教程
│   ├── 00_快速开始.md
│   ├── 01_Vivado工程创建指南.md
│   ├── 02_XDC约束文件详解.md
│   ├── 03_Verilog基础语法.md
│   └── 04_时序逻辑与FSM.md
│
├── constraints/                       # XDC 约束文件
│   ├── board_pinout.xdc              # 开发板引脚定义
│   └── timing.xdc                    # 时序约束
│
├── common/                            # 通用模块库
│   ├── clk_div.v                     # 时钟分频器
│   ├── debounce.v                    # 按键消抖
│   ├── edge_detect.v                 # 边沿检测
│   ├── fifo.v                        # FIFO 缓冲区
│   └── uart_base.v                   # UART 基础模块
│
├── 01_led_blink/
│   ├── led_blink.v
│   ├── led_blink_tb.v
│   └── README.md
│
├── 02_button_led/
│   ├── button_led.v
│   ├── button_led_tb.v
│   └── README.md
│
├── 03_key_counter/
│   ├── key_counter.v
│   ├── key_counter_tb.v
│   └── README.md
│
├── 04_seg_display/
│   ├── seg_display.v
│   ├── seg_display_tb.v
│   └── README.md
│
├── 05_traffic_light/
│   ├── traffic_light.v
│   ├── traffic_light_tb.v
│   └── README.md
│
├── 06_pwm_breathing/
│   ├── pwm_breathing.v
│   ├── pwm_breathing_tb.v
│   └── README.md
│
├── 07_uart_rx/
│   ├── uart_rx.v
│   ├── uart_rx_tb.v
│   └── README.md
│
├── 08_uart_txrx/
│   ├── uart_tx.v
│   ├── uart_rx.v
│   ├── uart_txrx.v
│   ├── uart_txrx_tb.v
│   └── README.md
│
├── 09_beeper/
│   ├── beeper.v
│   ├── beeper_tb.v
│   └── README.md
│
├── 10_touch_key/
│   ├── touch_key.v
│   ├── touch_key_tb.v
│   └── README.md
│
├── 11_vga_display/
│   ├── vga_controller.v
│   ├── vga_controller_tb.v
│   ├── pixel_gen.v
│   └── README.md
│
├── 12_lcd_display/
│   ├── lcd_controller.v
│   ├── lcd_controller_tb.v
│   ├── lcd_driver.v
│   └── README.md
│
├── 13_hdmi_output/
│   ├── hdmi_controller.v
│   ├── tmds_encoder.v
│   ├── hdmi_controller_tb.v
│   └── README.md
│
├── 14_camera_capture/
│   ├── camera_controller.v
│   ├── sccb_master.v
│   ├── camera_capture_tb.v
│   └── README.md
│
├── 15_image_sobel/
│   ├── sobel_filter.v
│   ├── sobel_filter_tb.v
│   ├── line_buffer.v
│   └── README.md
│
├── tools/                             # 工具脚本
│   ├── create_project.tcl             # Vivado TCL 脚本
│   └── simulate.sh                    # 仿真脚本
│
└── LICENSE
```

## 🔧 开发板规格

**50MHz Zynq-7020 开发板**

### 系统时钟
- `sys_clk` - U18 脚 - 50MHz 系统时钟

### 复位与按键
- `sys_rst_n` - N16 脚 - 低电平有效
- `key[0]` - L14 脚 - PL 按键 0
- `key[1]` - K16 脚 - PL 按键 1
- `touch_key` - F16 脚 - 触摸按键

### LED 输出
- `led[0]` - H15 脚 - 底板 LED 0
- `led[1]` - L15 脚 - 底板 LED 1
- `led` - J16 脚 - 核心板 LED

### 其他输出
- `beep` - M14 脚 - 蜂鸣器
- `gbc_led` - N15 脚 - 模块 LED

### 串口接口
- `uart_rxd` - K14 脚 - RS232 接收
- `uart_txd` - M15 脚 - RS232 发送
- `uart_rx` - T19 脚 - ATK 模块接收
- `uart_tx` - J15 脚 - ATK 模块发送

### LCD 接口
- RGB TFT-LCD: `lcd_*` 系列引脚 - 支持 24 位真彩色

### HDMI 接口
- TMDS 差分信号：`tmds_data_p[0:2]`、`tmds_clk_p`

### 摄像头接口
- OV5640/OV7725：`cam_*` 系列引脚 - 支持 8 位数据

### 其他接口
- I²C：`iic_scl`、`iic_sda` - E18、F17
- CAN：`can_rx`、`can_tx` - L16、J14
- 以太网：`eth_*` 系列引脚
- 音频：`aud_*` 系列引脚

## 🚀 快速开始

### 1. 环境准备

```bash
# 克隆仓库
git clone https://github.com/akashappigadu-dev/zynq7020-pl-verilog-projects.git
cd zynq7020-pl-verilog-projects

# 所需工具
- Vivado 2020.1 或更高版本
- ModelSim/Questa（可选，用于仿真）
```

### 2. 运行第一个项目（LED 闪烁）

```bash
cd 01_led_blink

# 使用 Vivado 创建工程
vivado -mode batch -source ../tools/create_project.tcl -tclargs 01_led_blink

# 或手动步骤：
# 1. 打开 Vivado
# 2. File → New Project
# 3. 选择 Zynq-7020 芯片
# 4. 添加源文件：led_blink.v
# 5. 添加约束文件：../constraints/board_pinout.xdc
# 6. 综合、实现、生成 bitstream
```

### 3. 运行仿真

```bash
# 使用 iverilog + GTKWave
iverilog -o led_blink_sim led_blink.v led_blink_tb.v
vvp led_blink_sim
gtkwave led_blink.vcd
```

### 4. 烧写到开发板

```bash
# 在 Vivado 中
# 1. 连接开发板
# 2. Tools → Program and Debug → Program Device
# 3. 选择生成的 .bit 文件
# 4. 点击 Program
```

## 📚 学习资源

### 推荐阅读顺序

1. **docs/00_快速开始.md** - 环境配置
2. **docs/01_Vivado工程创建指南.md** - Vivado 基础
3. **docs/02_XDC约束文件详解.md** - 引脚配置
4. **docs/03_Verilog基础语法.md** - 语言基础
5. **docs/04_时序逻辑与FSM.md** - 高级概念

### 外部资源

- [Xilinx 官方文档](https://docs.xilinx.com)
- [Zynq-7020 技术参考手册](https://www.xilinx.com/support/documentation/user_guides/ug585-zynq-7000-trm.pdf)
- [Verilog HDL 教程](https://www.chipverify.com/verilog/verilog-tutorial)
- [数字逻辑设计基础](https://en.wikibooks.org/wiki/Digital_Circuits)

## 💡 学习建议

### ✅ 推荐做法

- 先理解项目的**功能需求**
- 阅读注释理解**架构设计**
- 自己尝试**修改参数**
- 运行**仿真测试**
- 在开发板上**实际验证**
- 尝试**功能扩展**

### ❌ 避免做法

- 不要直接复制粘贴不理解
- 不要跳过仿真直接烧写
- 不要忽视 XDC 约束文件
- 不要一次改太多代码

## 🤝 贡献指南

欢迎提交 Pull Request 或 Issue：

- 发现 Bug？提交 Issue
- 有更优秀的实现？提交 PR
- 想添加新项目？欢迎讨论

## 📝 许可证

MIT License - 可自由使用和修改

## 🙏 致谢

感谢所有贡献者和使用者的支持！

---

## 📞 联系方式

如有问题，欢迎通过以下方式联系：

- GitHub Issues
- 邮件讨论

---

**祝你学习愉快！🎉**

希望这套项目能帮助你从零开始学习 FPGA 设计！
