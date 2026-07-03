# MOSFET跨导小信号与频率限制

标签：#MOSFET #跨导 #小信号模型 #截止频率 #Chapter10

## 一句话理解

MOSFET 的放大能力由跨导（transconductance）$g_m$ 描述，频率上限主要由栅电容充放电决定，而不是载流子穿过沟道的时间。

## 跨导定义

跨导表示栅源电压微小变化引起漏电流变化的能力：

$$
g_m=\frac{\partial I_D}{\partial V_{GS}}
$$

在线性区：

$$
g_m=k_n\frac{W}{L}V_{DS}
$$

在饱和区：

$$
g_m=k_n\frac{W}{L}(V_{GS}-V_T)
$$

也可用饱和电流表示：

$$
g_m=\sqrt{2k_n\frac{W}{L}I_D}
$$

## 衬底偏置效应

当源-衬底反偏 $V_{SB}$ 增大时，阈值电压升高。n 沟道 MOSFET 的体效应近似为：

$$
V_T=V_{T0}+\gamma\left[\sqrt{2\phi_{fp}+V_{SB}}-\sqrt{2\phi_{fp}}\right]
$$

其中体效应系数（body-effect coefficient）：

$$
\gamma=\frac{\sqrt{2e\varepsilon_sN_A}}{C'_{ox}}
$$

物理图像：源-衬底反偏增大耗尽层电荷，栅极需要更高电压才能达到同样反型条件。

> [!figure] Fig-10-51 占位
> 衬底偏置对阈值电压和转移特性的影响。

## 小信号等效电路

MOSFET 小信号模型包含：

- 受控电流源 $g_m v_{gs}$。
- 输出电阻 $r_{ds}$。
- 栅源电容 $C_{gs}$。
- 栅漏电容 $C_{gd}$。
- 源 / 漏串联电阻 $r_s$、$r_d$。
- 漏-衬底结电容 $C_{ds}$。

> [!figure] Fig-10-52 占位
> MOSFET 内在电阻、电容和受控源的小信号模型。

源串联电阻会降低有效跨导：

$$
g'_m=\frac{g_m}{1+g_mr_s}
$$

## 频率限制

两类频率限制：

1. 沟道渡越时间（channel transit time）：通常不是主要限制。
2. 栅电容充放电时间：通常是主要限制。

栅漏电容会通过米勒效应（Miller effect）放大为：

$$
C_M=C_{gdT}(1+g_mR_L)
$$

因此漏端重叠电容会显著降低高频响应。

## 截止频率

截止频率（cutoff frequency）定义为电流增益幅值为 1 的频率：

$$
f_T=\frac{g_m}{2\pi(C_{gsT}+C_M)}
$$

若忽略寄生电容、MOSFET 工作在理想饱和区且 $C_G\approx C'_{ox}WL$，则：

$$
f_T\approx\frac{\mu_n(V_{GS}-V_T)}{2\pi L^2}
$$

所以缩短沟道长度 $L$ 能显著提高频率响应。

## 易错点

- 栅极直流输入电阻很大，但高频输入阻抗不无限大，因为栅电容要充放电。
- $C_{gd}$ 在共源放大中通过米勒效应被放大，常比单纯数值看起来更重要。
- 源电阻负反馈会降低有效跨导。
- 理想长沟道公式预测 $f_T\propto 1/L^2$，实际短沟道会受到速度饱和和寄生电容限制。

## 连接

- 前接 [[MOSFET理想IV方程]]。
- 后接 [[迁移率退化速度饱和与弹道输运]] 和 [[MOSFET缩放]]。
