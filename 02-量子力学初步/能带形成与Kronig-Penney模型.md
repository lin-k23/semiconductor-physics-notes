# 能带形成与Kronig-Penney模型

标签：#能带理论 #KronigPenney #BlochTheorem #Chapter3

## 一句话理解

当许多 atoms 靠近形成 crystal 时，原本离散的 atomic energy levels 因 wave functions overlap 与 Pauli exclusion principle 而分裂成大量 closely spaced levels，宏观上表现为 allowed energy bands，中间夹着 forbidden energy bands。

![Figure 3.3/3.4 Silicon band splitting](_assets/pdf-screenshots/fig3-4-silicon-band-splitting.png)

## 从单原子到晶体

Chapter 2 中 one-electron atom 的结论是：bound electron 只能取 discrete energy levels。若两个原子靠近，electron wave functions 会 overlap，两个电子会相互作用，原本一个 discrete level 会 split 成两个能级。

推广到 $N$ 个原子：

```text
one atomic level -> N closely spaced levels -> allowed energy band
```

由于 $N$ 非常大，相邻 levels 的间隔极小，所以 allowed band 内部常近似为 quasi-continuous distribution。

## Silicon 的 band splitting

对 isolated silicon atom：

- 内层 10 个电子 tightly bound。
- 外层 4 个 valence electrons 位于 $n=3$ shell。
- `3s` state 有 2 个 quantum states per atom。
- `3p` state 有 6 个 quantum states per atom。

当 Si atoms 靠近 equilibrium spacing $a_0$ 时，`3s` 和 `3p` states 发生 interaction and overlap，形成两个 bands：

- lower band：4N states，T = 0 K 时被 4N electrons 填满，即 valence band。
- upper band：4N states，T = 0 K 时 empty，即 conduction band。

二者之间的 forbidden band width 是 $E_g$。

## Kronig-Penney model

`Kronig-Penney model` 用一维 periodic potential function 近似 single-crystal lattice。

它的意义不是精确模拟真实三维晶体，而是展示：在 periodic potential 中解 Schrodinger equation 会自然得到 allowed bands 与 forbidden gaps。

## Bloch theorem

周期势场中的 one-electron wave function 可写成：

$$
\psi(x)=u(x)e^{jkx}
$$

其中：

- $u(x)$：periodic function，与 lattice period 相同。
- $k$：wave number，也称 crystal momentum 的相关参数。

加上时间因子：

$$
\Psi(x,t)=u(x)e^{j(kx-Et/\hbar)}
$$

这表示 electron 在 single-crystal material 中仍可用 traveling wave 形式描述，只是 wave amplitude 受到 periodic lattice 调制。

## E-k diagram 与 forbidden gaps

Kronig-Penney model 的结果给出 $E$ 与 $k$ 的关系。与 free electron 的 continuous parabola 不同，crystal 中的 $E(k)$ 出现 discontinuities，对应 forbidden energy gaps。

## 关键结论

- 能带不是人为假设，而是 quantum mechanics + periodic potential + boundary conditions 的结果。
- forbidden band 代表 Schrodinger equation 在这些能量上没有可接受解。
- bandgap energy $E_g$ 决定材料是 metal、semiconductor 还是 insulator 的重要因素。

## 易错点

- allowed band 内部仍由非常多 discrete quantum states 组成，只是间距极小。
- `k` 在 crystal 中不是普通 momentum，而是包含 lattice interaction 的 crystal momentum 参数。
- Kronig-Penney model 是一维理想模型，但揭示了能带形成的核心机制。
