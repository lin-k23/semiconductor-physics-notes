# MOSFET非理想效应总览

标签：#MOSFET #非理想效应 #短沟道 #Chapter11

来源：Chapter 11 *Metal–Oxide–Semiconductor Field-Effect Transistor: Additional Concepts*

## 本章一句话

Chapter 11 在 Chapter 10 的理想长沟道 MOSFET 模型上加入真实器件效应：亚阈值导电、沟道长度调制、迁移率退化、速度饱和、缩放、小尺寸阈值修正、击穿、离子注入调阈值以及辐射 / 热电子可靠性问题。

## 本章知识链

```text
理想 MOSFET 假设
  -> VGS < VT 时 ID=0，饱和区 ID 不随 VDS 变
  -> 实际：亚阈值电流 + 沟道长度调制
  -> 高场：迁移率退化 + 速度饱和 + 热载流子
  -> 尺寸缩小：短沟道 / 窄沟道阈值偏移
  -> 工艺控制：LDD、离子注入调阈值
  -> 可靠性：氧化层击穿、辐射电荷、界面态、热电子注入
```

## 必要图片占位

> [!figure] Fig-11-1
> ![Fig-11-1](_assets/pdf-screenshots/Fig-11-1.jpg)
> 理想与实验 $\sqrt{I_D}$-$V_{GS}$ 曲线对比，显示亚阈值电流。

> [!figure] Fig-11-5
> ![Fig-11-5](_assets/pdf-screenshots/Fig-11-5.jpg)
> 沟道长度调制：漏端耗尽区向沟道伸入，减小有效沟道长度。

> [!figure] Fig-11-11
> ![Fig-11-11](_assets/pdf-screenshots/Fig-11-11.jpg)
> 常数迁移率模型和速度饱和模型下的 $I_D$-$V_D$ 曲线对比。

> [!figure] Fig-11-20
> ![Fig-11-20](_assets/pdf-screenshots/Fig-11-20.jpg)
> 短沟道效应和窄沟道效应对阈值电压的相反影响。

> [!figure] Fig-11-35
> ![Fig-11-35](_assets/pdf-screenshots/Fig-11-35.jpg)
> 热电子产生、进入氧化层并引起器件退化的示意图。

## 本章核心问题

- 为什么 $V_{GS}<V_T$ 时仍然有漏电流？
- 饱和区为什么仍有有限输出电阻？
- 垂直电场和表面散射为什么会降低有效迁移率？
- 速度饱和为什么让 $I_D(sat)$ 从平方律变得近似线性？
- 常电场缩放为什么要求尺寸、氧化层厚度和电压同时缩小？
- 短沟道和窄沟道为什么对 $V_T$ 的影响方向相反？
- LDD 结构为什么能降低热载流子和击穿问题？
- 辐射和热电子为什么会改变阈值电压并降低迁移率？

## 与 Chapter 10 的关系

- Chapter 10：建立理想长沟道 MOSFET 模型。
- Chapter 11：解释实际器件偏离理想模型的原因，以及小尺寸器件中的设计权衡。

## 与后续器件的连接

- 功率 MOSFET 需要重点考虑击穿和安全工作区。
- 高速 MOSFET / CMOS 设计需要重点考虑速度饱和、寄生电容和热载流子可靠性。
- HEMT / 异质结器件会借助 [[二维电子气]] 改善迁移率与高频性能。
