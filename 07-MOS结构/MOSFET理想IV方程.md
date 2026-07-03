# MOSFET理想IV方程

标签：#MOSFET #IV特性 #线性区 #饱和区 #Chapter10

## 一句话理解

理想长沟道 MOSFET 的 I-V 方程来自两个近似：沟道电荷由局部栅压超过阈值的部分决定，沟道电流由该反型电荷在横向电场中漂移形成。

## 沟道电荷近似

沿沟道取位置 $x$，局部沟道电势为 $V_x$。n 沟道增强型 MOSFET 中，单位面积反型层电荷近似为：

$$
Q'_n(x)=-C'_{ox}\left[(V_{GS}-V_x)-V_T\right]
$$

只要 $V_{GS}-V_x>V_T$，该处存在反型沟道。

> [!figure] Fig-10-46 占位
> 沟道位置 $x$ 处的电势和 MOS 能带关系。

## 线性区电流

沟道电流由漂移电流给出：

$$
I_D=W\mu_n C'_{ox}\left[(V_{GS}-V_T)-V_x\right]\frac{dV_x}{dx}
$$

从源端 $V_x=0$ 积分到漏端 $V_x=V_{DS}$，得到：

$$
I_D=\frac{W\mu_n C'_{ox}}{2L}\left[2(V_{GS}-V_T)V_{DS}-V_{DS}^2\right]
$$

定义工艺电导参数：

$$
k_n=\mu_n C'_{ox}
$$

则：

$$
I_D=\frac{k_n}{2}\frac{W}{L}\left[2(V_{GS}-V_T)V_{DS}-V_{DS}^2\right]
$$

适用条件：

$$
0\le V_{DS}\le V_{GS}-V_T
$$

## 饱和区电流

当 $V_{DS}=V_{GS}-V_T$ 时，漏端沟道电荷为零，进入饱和区：

$$
V_{DS}(sat)=V_{GS}-V_T
$$

饱和电流：

$$
I_D(sat)=\frac{k_n}{2}\frac{W}{L}(V_{GS}-V_T)^2
$$

理想模型中，当 $V_{DS}\ge V_{DS}(sat)$，$I_D$ 与 $V_{DS}$ 无关。

> [!figure] Fig-10-47 占位
> 理想 $I_D$-$V_{DS}$ 曲线族。

## 小 $V_{DS}$ 下的沟道电阻

当 $V_{DS}$ 很小时，$V_{DS}^2$ 项可忽略：

$$
I_D\approx k_n\frac{W}{L}(V_{GS}-V_T)V_{DS}
$$

因此沟道电导为：

$$
g_d\approx k_n\frac{W}{L}(V_{GS}-V_T)
$$

栅压越大，沟道电导越大，等效电阻越小。

## p 沟道公式使用建议

p 沟道 MOSFET 的公式可用幅值写法记忆：

$$
|I_D(sat)|=\frac{k_p}{2}\frac{W}{L}(|V_{GS}|-|V_T|)^2
$$

考试中要特别注意电压极性和电流方向。

## 易错点

- 饱和条件来自漏端局部栅压刚好等于阈值：$V_{GS}-V_{DS}=V_T$。
- 理想饱和区 $I_D$ 不随 $V_{DS}$ 变，但实际器件会有沟道长度调制，见 [[沟道长度调制与输出电阻]]。
- $k_n$ 是工艺相关参数，$K_n=(k_n/2)(W/L)$ 是器件几何也包含进去后的电导参数。
- 线性区不是简单欧姆电阻；沟道电荷沿 $x$ 方向会随 $V_x$ 变化。

## 连接

- 前接 [[MOSFET结构与工作区]]。
- 后接 [[MOSFET跨导小信号与频率限制]] 和 Chapter 11 的 [[MOSFET非理想效应总览]]。
