# BJT少数载流子分布与电流

标签：#BJT #少数载流子 #扩散电流 #正向有源区 #Chapter12

## 一句话理解

BJT 的集电极电流来自基区少数载流子浓度梯度：B-E 正偏把电子注入基区，B-C 反偏把集电端边界少数电子浓度拉低到近似零，于是基区中形成近似线性的电子浓度分布，扩散电流被集电极收集。

## 正向有源区边界条件

以 npn BJT 为例，基区是 p 型，电子是基区少数载流子。

B-E 结正偏：

$$
\Delta n_B(0)=n_{B0}\left[\exp\left(\frac{eV_{BE}}{kT}\right)-1\right]
$$

B-C 结反偏：

$$
\Delta n_B(x_B)=-n_{B0}
$$

其中 $x_B$ 是中性基区宽度，$n_{B0}$ 是基区热平衡少数电子浓度。

> [!figure] Fig-12-13 占位
> npn BJT 中性发射区、基区、集电区坐标定义。

> [!figure] Fig-12-14 占位
> 正向有源区中三段少数载流子分布。

## 基区少数载流子分布

稳态、零电场条件下，基区过剩电子满足：

$$
D_B\frac{d^2\Delta n_B(x)}{dx^2}-\frac{\Delta n_B(x)}{\tau_{B0}}=0
$$

一般解为双曲函数形式。若基区很窄：

$$
x_B\ll L_B
$$

则 $\sinh(x/L_B)\approx x/L_B$，基区少数载流子近似线性：

$$
\Delta n_B(x)\approx \frac{n_{B0}}{x_B}\left[\left(\exp\left(\frac{eV_{BE}}{kT}\right)-1\right)(x_B-x)-x\right]
$$

复习图像：窄基区让电子大概率穿过基区，而不是在基区内复合。

> [!figure] Fig-12-15 占位
> 双曲正弦函数和线性近似。

## 集电极电流

若忽略基区复合，基区电子浓度近似从 $n_B(0)$ 线性降到 0，集电极电流可写为：

$$
i_C\approx eD_BA\frac{n_B(0)}{x_B}
$$

利用 B-E 正偏边界条件：

$$
i_C\approx \frac{eD_BA}{x_B}n_{B0}\exp\left(\frac{V_{BE}}{V_T}\right)
$$

所以：

$$
i_C=I_S\exp\left(\frac{V_{BE}}{V_T}\right)
$$

这就是 BJT 的核心控制关系。

## 发射区和集电区少数载流子

发射区中的少数空穴由 B-E 正偏注入，若发射区长度有限：

$$
\Delta p_E(x')=p_{E0}\left[\exp\left(\frac{eV_{BE}}{kT}\right)-1\right]\frac{\sinh\left(\frac{x_E-x'}{L_E}\right)}{\sinh\left(\frac{x_E}{L_E}\right)}
$$

集电区在 B-C 反偏下，边界少数空穴浓度近似被抽空：

$$
\Delta p_C(x'')=-p_{C0}\exp\left(-\frac{x''}{L_C}\right)
$$

## 其他工作模式的分布图像

- 截止（cutoff）：两个结都反偏，基区少数载流子被抽空。
- 饱和（saturation）：两个结都正偏，基区两端都有过剩少数载流子。
- 反向有源（inverse active）：由集电极向基区注入电子，但由于结构非对称，性能较差。

> [!figure] Fig-12-16 占位
> 截止和饱和模式的少数载流子分布。

> [!figure] Fig-12-17 占位
> 反向有源模式的少数载流子分布。

## 易错点

- BJT 的 $i_C$ 不是“集电极主动发射”的电流，而是发射极注入、基区扩散、集电极收集的结果。
- 基区少数载流子分布近似线性依赖 $x_B\ll L_B$，基区太宽时复合显著增加。
- 集电极电流与 B-C 反偏强度理想上无关，但只在 B-C 结保持反偏并且未击穿时成立。
- 发射极重掺杂是为了让电子注入基区远大于空穴注入发射区。

## 连接

- 来自 [[05-非平衡载流子/低注入与少数载流子控制]]。
- 来自 [[06-PN结/少数载流子分布与理想二极管方程]]。
- 后续 [[BJT电流增益非理想效应]] 会讨论这些分布如何决定 $\alpha$ 和 $\beta$。
