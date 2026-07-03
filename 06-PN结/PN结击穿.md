# PN结击穿

标签：#PN结 #击穿 #雪崩击穿 #齐纳击穿 #Chapter7

## 一句话理解

PN 结的反向偏置不能无限增大；当反向电场足够强时，会出现齐纳击穿（Zener breakdown）或雪崩击穿（avalanche breakdown），导致反向电流急剧增加。

![Figure 7.12 and 7.13 Breakdown mechanisms](_assets/pdf-screenshots/fig7-12-13-breakdown-mechanisms.png)

## 两种击穿机制

### 齐纳击穿（Zener breakdown）

齐纳击穿发生在高掺杂 PN 结中。高掺杂使耗尽区很窄，反偏时 p 侧价带和 n 侧导带在空间上非常接近，电子可以通过隧穿（tunneling）从 p 侧价带进入 n 侧导带。

特点：

- 高掺杂。
- 窄耗尽区。
- 隧穿机制。
- 通常发生在较低击穿电压。

### 雪崩击穿（avalanche breakdown）

雪崩击穿发生在较宽的耗尽区中。载流子在强电场中获得足够动能，通过碰撞电离（impact ionization）产生新的电子-空穴对，新载流子继续加速并产生更多电子-空穴对，形成倍增过程（multiplication）。

特点：

- 电场强。
- 通过碰撞电离产生电子-空穴对。
- 常是一般 PN 结的主要击穿机制。

## 雪崩倍增条件

若电子电离率和空穴电离率近似相等：

$$
\alpha_n=\alpha_p=\alpha
$$

雪崩击穿条件可写成：

$$
\int_0^W \alpha\,dx=1
$$

实际中 $\alpha$ 强烈依赖电场，而电场在耗尽区中并非常数，所以精确计算较复杂。

## 单边结击穿电压近似

![Figure 7.14 Critical electric field at breakdown](_assets/pdf-screenshots/fig7-14-critical-field.png)

对单边突变结，若忽略 $V_{bi}$，令击穿时最大电场达到临界电场（critical electric field）$E_{crit}$，则：

$$
V_B=\frac{\epsilon_sE_{crit}^2}{2eN_B}
$$

其中 $N_B$ 是低掺杂侧浓度。

## 击穿电压与掺杂

![Figure 7.15 Breakdown voltage versus impurity concentration](_assets/pdf-screenshots/fig7-15-breakdown-voltage.png)

击穿电压随低掺杂侧浓度降低而增大：

```text
low-doped region concentration decreases
  -> depletion width increases
  -> same voltage gives lower peak field
  -> breakdown voltage increases
```

## 易错点

- 齐纳击穿和雪崩击穿都发生在反向偏置下，但机制不同。
- 高掺杂更容易产生齐纳隧穿。
- 击穿不是材料“烧坏”的同义词；如果限流得当，击穿可以是可逆工作状态。
