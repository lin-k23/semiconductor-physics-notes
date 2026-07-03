# 零偏PN结与内建电势

标签：#PN结 #内建电势 #费米能级 #Chapter7

## 一句话理解

零偏 PN 结处于热平衡（thermal equilibrium），整个结构的费米能级（Fermi level）必须恒定；导带和价带的弯曲对应内建电势（built-in potential barrier）$V_{bi}$。

## 热平衡能带图

零偏（zero applied bias）时，PN 结没有外加激发，满足：

$$
E_F=\text{constant}
$$

p 区和 n 区的费米能级相对于本征费米能级（intrinsic Fermi level）位置不同，因此导带（conduction band）和价带（valence band）必须在耗尽区内弯曲。

## 内建电势的物理意义

内建电势（built-in potential）是多数载流子跨越 PN 结时看到的势垒：

- n 区电子进入 p 区需要越过势垒。
- p 区空穴进入 n 区也需要越过势垒。
- 这个势垒维持热平衡，抵消多数载流子的扩散趋势。

注意：$V_{bi}$ 不能直接用外接电压表测量，因为金属探针与半导体接触处会形成额外接触电势并抵消测量值。

## 内建电势公式

对非简并、完全电离的突变 PN 结：

$$
V_{bi}=V_T\ln\left(\frac{N_A N_D}{n_i^2}\right)
$$

其中：

$$
V_T=\frac{kT}{e}
$$

称为热电压（thermal voltage）。在 300 K：

$$
V_T\approx 0.0259\ \text{V}
$$

## 推导线索

n 区：

$$
n_0=n_i\exp\left(\frac{E_F-E_{Fi}}{kT}\right)\approx N_D
$$

p 区：

$$
p_0=n_i\exp\left(\frac{E_{Fi}-E_F}{kT}\right)\approx N_A
$$

将 p 区和 n 区的本征能级差相加即可得到：

$$
V_{bi}=\frac{kT}{e}\ln\left(\frac{N_A N_D}{n_i^2}\right)
$$

## 近似条件

该公式依赖：

- 玻尔兹曼近似（Boltzmann approximation）有效。
- 掺杂非简并（nondegenerate doping）。
- 杂质完全电离（complete ionization）。
- $N_A$ 与 $N_D$ 表示各自区域的净受主 / 施主浓度。

## 易错点

- $V_{bi}$ 随掺杂浓度呈对数变化，因此掺杂改变几个数量级，$V_{bi}$ 变化也相对有限。
- $V_{bi}$ 是内部势垒，不是外加电压。
- 热平衡下费米能级恒定，但导带和价带会弯曲。
