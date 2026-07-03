# 介电弛豫与Haynes-Shockley实验

标签：#非平衡载流子 #DielectricRelaxation #HaynesShockley #Chapter6

## 一句话理解

`dielectric relaxation time constant` 说明局部净电荷会极快被中和，因此 quasi-neutrality 假设通常合理；`Haynes-Shockley experiment` 则通过一个 excess carrier pulse 同时测量 mobility、diffusion coefficient 和 lifetime。

## Dielectric relaxation

若 semiconductor 中突然注入一小块净 charge density $\rho$，由 Poisson equation、Ohm's law 和 continuity equation：

$$
\nabla\cdot E=\frac{\rho}{\epsilon}
$$

$$
J=\sigma E
$$

$$
\nabla\cdot J=-\frac{\partial \rho}{\partial t}
$$

可得：

$$
\frac{d\rho}{dt}+\frac{\sigma}{\epsilon}\rho=0
$$

解为：

$$
\rho(t)=\rho(0)e^{-t/\tau_d}
$$

其中：

$$
\tau_d=\frac{\epsilon}{\sigma}
$$

## 物理意义

在常见掺杂 semiconductor 中，$\tau_d$ 通常远小于 excess carrier lifetime。也就是说，局部净电荷会在极短时间内被拉平，因此可以近似使用 charge neutrality：

$$
\delta n\approx\delta p
$$

## Haynes-Shockley experiment

实验结构：

1. 在 contact A 注入短 pulse 的 excess carriers。
2. applied electric field 使 pulse drift 到 contact B。
3. contact B 收集部分 carriers，输出 pulse voltage。

由 arrival time $t_0$ 可求 minority carrier mobility：

$$
\mu_p=\frac{d}{E_0t_0}
$$

由 pulse width $\Delta t=t_2-t_1$ 可估算 diffusion coefficient：

$$
D_p=\frac{(\mu_pE_0)^2(\Delta t)^2}{16t_0}
$$

由不同 electric field 下 pulse area $S$ 的衰减可求 lifetime：

$$
S=K\exp\left[-\frac{d}{\mu_pE_0\tau_{p0}}\right]
$$

## 易错点

- dielectric relaxation 处理的是 net charge density，不是 electron-hole recombination。
- quasi-neutrality 快速建立，不代表 carriers 已经 recombined。
- Haynes-Shockley 同时观察 drift、diffusion、recombination 三个过程。
