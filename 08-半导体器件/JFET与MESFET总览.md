# JFET与MESFET总览

标签：#JFET #MESFET #场效应晶体管 #HEMT #Chapter13

来源：Chapter 13 *The Junction Field-Effect Transistor*

## 本章一句话

结型场效应晶体管（junction field-effect transistor, JFET）用反偏 PN 结或肖特基势垒结产生的空间电荷区调制导电沟道宽度，从而用栅压控制漏电流；它是多数载流子参与导电的单极型晶体管（unipolar transistor）。

## 本章知识链

```text
场效应：垂直电场调制沟道电导
  -> pn JFET：反偏 PN 结扩大耗尽区
  -> MESFET：反偏肖特基栅扩大耗尽区
  -> 栅压控制有效沟道厚度
  -> 夹断、饱和和漏电流公式
  -> 跨导、小信号模型和频率响应
  -> 非理想效应：沟道长度调制、速度饱和
  -> HEMT：异质结二维电子气沟道
```

## 必要图片占位

> [!figure] Fig-13-2 占位
> 对称 n 沟道 pn JFET 结构。

> [!figure] Fig-13-3 占位
> 不同反向栅压下的沟道耗尽区和小 $V_{DS}$ I-V 特性。

> [!figure] Fig-13-6 占位
> n 沟道 MESFET 结构。

> [!figure] Fig-13-22 占位
> JFET 理想输出特性族。

> [!figure] Fig-13-33 占位
> HEMT 的异质结和二维电子气沟道结构。

## 本章核心问题

- JFET 为什么是“正常导通”（normally on）的耗尽型器件？
- 栅压如何通过空间电荷区改变沟道厚度和沟道电阻？
- 夹断（pinchoff）为什么不等于漏电流为零？
- 内部夹断电压 $V_{p0}$、夹断电压 $V_p$ 和 $V_{DS}(sat)$ 有什么区别？
- pn JFET 和 MESFET 的栅结构差别是什么？
- MESFET 为什么常用 GaAs 和半绝缘衬底？
- JFET 的跨导、输出电阻和频率响应受哪些几何参数控制？
- HEMT 为什么能获得高迁移率和高频性能？

## 和前后章节的连接

- 来自 [[06-PN结/反向偏置PN结]]：pn JFET 的栅控来自反偏 PN 结耗尽层。
- 来自 [[07-MOS结构/金属半导体结与异质结]]：MESFET 的栅极是肖特基势垒结。
- 来自 [[07-MOS结构/二维电子气]]：HEMT 用异质结 2-DEG 作为高迁移率沟道。
- 对比 [[07-MOS结构/MOSFET结构与工作区]]：MOSFET 用氧化层栅电场控制反型沟道，JFET 用反偏结耗尽层控制已有沟道。
