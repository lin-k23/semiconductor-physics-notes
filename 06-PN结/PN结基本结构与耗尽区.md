# PN结基本结构与耗尽区

标签：#PN结 #耗尽区 #空间电荷区 #Chapter7

## 一句话理解

PN 结的核心结构是冶金结（metallurgical junction）附近形成的空间电荷区 / 耗尽区（space charge region / depletion region）；该区域几乎没有可移动电子和空穴，只剩固定离化杂质电荷。

![Figure 7.1 and 7.2 Basic PN junction and space charge region](_assets/pdf-screenshots/fig7-1-2-basic-pn-junction-and-space-charge.png)

## 基本结构

PN 结并不是把两块独立半导体简单贴在一起，而是在同一单晶材料中形成相邻的 p 型区和 n 型区：

- p 型区：主要掺受主（acceptor）杂质，平衡多数载流子为空穴。
- n 型区：主要掺施主（donor）杂质，平衡多数载流子为电子。
- 两区交界面称为冶金结（metallurgical junction）。

理想均匀掺杂 PN 结常用阶跃结（step junction）近似：

```text
x < 0: p region, acceptor concentration Na
x > 0: n region, donor concentration Nd
x = 0: metallurgical junction
```

## 空间电荷区如何形成？

初始接触后，冶金结附近有很大的载流子浓度梯度：

- n 区多数电子向 p 区扩散。
- p 区多数空穴向 n 区扩散。

电子离开 n 区后留下固定的正电离化施主 $N_D^+$；空穴离开 p 区后留下固定的负电离化受主 $N_A^-$。这些固定电荷形成空间电荷区。

## 耗尽区近似

空间电荷区中可移动电子和空穴几乎被电场扫出，因此也称耗尽区（depletion region）。在突变耗尽近似（abrupt depletion approximation）中：

- 耗尽区内只有固定离化杂质电荷。
- 耗尽区外为电中性中性区（neutral region）。
- 耗尽区边界是 abrupt 的。

## 扩散力与电场力平衡

空间电荷区中的电场方向从 n 区指向 p 区。对多数载流子：

- 扩散趋势推动 electrons 从 n 到 p，holes 从 p 到 n。
- 电场力阻止这些多数载流子继续跨越耗尽区。

热平衡时：

```text
diffusion tendency = electric-field force
net current = 0
```

## 关键术语

- 冶金结（metallurgical junction）
- 空间电荷区（space charge region）
- 耗尽区（depletion region）
- 突变耗尽近似（abrupt depletion approximation）
- 阶跃结（step junction）

## 易错点

- 耗尽区不是没有电荷，而是没有可移动电荷；固定离化杂质电荷仍然存在。
- PN 结中的内建电场不是外加电场，而是由扩散后留下的固定空间电荷产生。
- 热平衡下有内建电势，但没有净电流。
