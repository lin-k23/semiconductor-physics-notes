# 过剩载流子寿命与SRH复合

标签：#非平衡载流子 #SRH #ShockleyReadHall #Lifetime #Chapter6

## 一句话理解

真实 semiconductor 中 defects 会在 bandgap 内引入 trap states 或 recombination centers；`Shockley-Read-Hall recombination` 描述 carriers 通过这些 midgap states 复合，因此 trap density 越高，excess carrier lifetime 越短。

![Figure 6.16 SRH trap processes](_assets/pdf-screenshots/fig6-16-srh-trap-processes.png)

## 四个基本过程

对 acceptor-type trap：

1. electron capture：empty trap 从 conduction band 捕获 electron。
2. electron emission：filled trap 向 conduction band 发射 electron。
3. hole capture：filled trap 捕获 hole，等效为 electron 从 trap 跳到 valence band。
4. hole emission：empty trap 向 valence band 发射 hole，等效为从 valence band 捕获 electron。

## Capture and emission rates

Electron capture：

$$
R_{cn}=C_nN_t[1-f_F(E_t)]n
$$

Electron emission：

$$
R_{en}=E_nN_tf_F(E_t)
$$

thermal equilibrium 中二者相等，可得：

$$
E_n=n'C_n
$$

其中：

$$
n'=N_c\exp\left[-\frac{E_c-E_t}{kT}\right]
$$

同理：

$$
p'=N_v\exp\left[-\frac{E_t-E_v}{kT}\right]
$$

## SRH recombination rate

一般形式：

$$
R=\frac{C_nC_pN_t(np-n_i^2)}{C_n(n+n')+C_p(p+p')}
$$

若用 lifetime 表示：

$$
R=\frac{np-n_i^2}{\tau_{p0}(n+n')+\tau_{n0}(p+p')}
$$

## Extrinsic + low injection limit

n-type semiconductor：

$$
R\approx C_pN_t\delta p=\frac{\delta p}{\tau_{p0}}
$$

$$
\tau_{p0}=\frac{1}{C_pN_t}
$$

p-type semiconductor：

$$
R\approx C_nN_t\delta n=\frac{\delta n}{\tau_{n0}}
$$

$$
\tau_{n0}=\frac{1}{C_nN_t}
$$

## 物理意义

- recombination rate 与 trap density $N_t$ 成正相关。
- lifetime 与 $N_t$ 成反比。
- midgap traps 通常最有效，因为它们能同时较容易捕获 electrons 和 holes。

## 易错点

- SRH recombination 不是 direct band-to-band recombination。
- trap state 在 bandgap 内，可能来自 crystal defects 或 impurities。
- extrinsic low injection 下，lifetime 仍归结为 minority carrier lifetime。
