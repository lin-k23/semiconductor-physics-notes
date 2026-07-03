# 非均匀掺杂PN结

标签：#PN结 #非均匀掺杂 #LinearlyGradedJunction #HyperabruptJunction #Chapter7

## 一句话理解

实际 PN 结常不是理想均匀掺杂；线性渐变结（linearly graded junction）和超突变结（hyperabrupt junction）会改变电场、电势和结电容的电压依赖，可用于特定器件设计。

## 线性渐变结

若净掺杂浓度在冶金结附近近似线性变化：

$$
\rho(x)=eax
$$

其中 $a$ 是净杂质浓度梯度（net impurity concentration gradient）。

由泊松方程：

$$
\frac{dE}{dx}=\frac{eax}{\epsilon_s}
$$

积分可知，线性渐变结中的电场是二次函数，而不是均匀掺杂突变结中的线性函数。

## 势垒与耗尽宽度

若耗尽区从 $-x_0$ 到 $+x_0$，零偏时：

$$
V_{bi}=\frac{2}{3}\frac{ea x_0^3}{\epsilon_s}
$$

反向偏置时，把 $V_{bi}$ 替换为 $V_{bi}+V_R$：

$$
x_0=\left[\frac{3\epsilon_s(V_{bi}+V_R)}{2ea}\right]^{1/3}
$$

## 线性渐变结电容

单位面积结电容：

$$
C'=\left[\frac{ea\epsilon_s^2}{12(V_{bi}+V_R)}\right]^{1/3}
$$

因此：

$$
C'\propto (V_{bi}+V_R)^{-1/3}
$$

相比均匀掺杂突变结的 $-1/2$ 次幂关系，线性渐变结的电容对反向偏置电压依赖更弱。

## 超突变结

超突变结（hyperabrupt junction）是一类非均匀掺杂结，其掺杂浓度从冶金结向外迅速降低。常用近似：

$$
N(x)=Bx^m
$$

当 $m<0$ 时，即为 hyperabrupt profile。

## 变容二极管应用

变容二极管（varactor diode）利用结电容随反向偏置电压变化的特性。若把变容二极管与电感并联，谐振频率为：

$$
f_r=\frac{1}{2\pi\sqrt{LC}}
$$

通过设计特定掺杂剖面，可以让电容-电压关系满足电路所需的调谐特性。

## 易错点

- 非均匀掺杂结的电场不再是简单线性函数。
- 线性渐变结的电容与电压关系是 $-1/3$ 次幂，而突变均匀结是 $-1/2$ 次幂。
- 超突变结不是“更突变”的阶跃结，而是指掺杂浓度向外快速变化的特殊剖面。
