# PN结二极管

标签：#PN结 #PN结二极管 #pnJunctionDiode #Chapter8

来源：Chapter 8 *The pn Junction Diode*

## 本章一句话

PN 结二极管（pn junction diode）是在 PN 结上施加偏置并产生电流的器件；正向偏置（forward bias）降低势垒，使多数载流子跨越空间电荷区并成为对侧的过剩少数载流子，随后通过扩散（diffusion）和复合（recombination）决定二极管电流。

## 本章知识链

```text
正向偏置降低势垒
  -> 多数载流子跨越空间电荷区
  -> 在对侧形成过剩少数载流子
  -> 少数载流子扩散 + 复合
  -> 理想二极管方程
  -> 非理想电流：产生电流 / 复合电流 / 高注入
  -> 小信号模型：rd、Cd、Cj、rs
  -> 电荷存储与开关瞬态
  -> 隧道二极管
```

## 视觉索引

![Figure 8.1 Bias energy bands](_assets/pdf-screenshots/fig8-1-bias-energy-bands.png)

![Figure 8.8 Ideal diode I-V](_assets/pdf-screenshots/fig8-8-ideal-diode-iv.png)

![Figure 8.16 Recombination, diffusion, and total current](_assets/pdf-screenshots/fig8-16-recombination-diffusion-total-current.png)

![Figure 8.19 Small-signal diffusion capacitance](_assets/pdf-screenshots/fig8-19-small-signal-diffusion-capacitance-qualitative.png)

![Figure 8.25 and 8.26 Turn-off transient](_assets/pdf-screenshots/fig8-25-26-turn-off-transient.png)

![Figure 8.29 Tunnel diode forward bias](_assets/pdf-screenshots/fig8-29a-c-tunnel-diode-forward-bias.png)

## 本章核心问题

- 正向偏置为什么会降低 PN 结势垒？
- 空间电荷区边界处的少数载流子浓度如何由外加电压决定？
- 为什么理想二极管电流由少数载流子扩散电流决定？
- 反向产生电流（generation current）和正向复合电流（recombination current）为什么导致非理想性？
- 高注入（high-level injection）如何改变 I-V 曲线斜率？
- 扩散电容（diffusion capacitance）和扩散电阻（diffusion resistance）来自什么物理过程？
- 正向转反向时为什么会有存储时间（storage time）？
- 隧道二极管（tunnel diode）的负微分电阻来自什么？

## 与前后章节的连接

- 来自 [[PN结]]：空间电荷区、势垒、电场和结电容。
- 来自 [[05-非平衡载流子/低注入与少数载流子控制]]：正向注入后用少数载流子扩散方程描述。
- 来自 [[05-非平衡载流子/准费米能级]]：正向偏置下 $E_{Fn}$ 与 $E_{Fp}$ 分离。
- 连接到后续 BJT 和光电器件：少数载流子注入、存储和复合是器件速度与效率的核心。
