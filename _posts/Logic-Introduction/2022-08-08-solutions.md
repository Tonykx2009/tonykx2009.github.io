---
title: 简明逻辑学：习题解答
layout: post
categories: 逻辑学简短入门
tags: 
  - 逻辑学
---

# 附录：习题解答

**第 1 章**：该推断不是演绎有效的。完全有可能前提为真，而乔塞是西班牙少数不是天主教徒的人。但是，前提一起对结论给出了很好的（尽管不是决定性的）支持理由。因此，该推断是归纳有效的。

**第 2 章**：令

> $$k$$ 为“琼斯是个流氓”
>
> $$f$$ 为“琼斯是个傻瓜”

则推断符号化为：

$$
\dfrac{k\lor f\quad k}{\neg f}
$$

真值表检测结果为：

| $$k$$ | $$f$$ | $$k\lor f$$ | $$k$$ | $$\neg f$$ |
| :---: | :---: | :---------: | :---: | :--------: |
| $$T$$ | $$T$$ |    $$T$$    | $$T$$ |   $$F$$    |
| $$T$$ | $$F$$ |    $$T$$    | $$T$$ |   $$T$$    |
| $$F$$ | $$T$$ |    $$T$$    | $$F$$ |   $$F$$    |
| $$F$$ | $$F$$ |    $$F$$    | $$F$$ |   $$T$$    |

第一行，两个前提都为 $$T$$，而结论为 $$F$$。因此，该推断是无效的。

**第 3 章**：令

> $$xS$$ 为“$$x$$ 看见枪击”
>
> $$xH$$ 为“$$x$$ 听见枪击”

令考虑中的对象为所有人。推断符号化为：

$$
\dfrac{\exists x(xS\lor xH)}{\exists x\ xS\lor \exists x\ xH}
$$

该推断是有效的。因为假设前提在某个情形为真，那就有某个对象 $$x$$ 在该情形的论域中使得 $$xS\lor xH$$ 为真。据 $$\lor$$ 的真值条件，$$xS$$ 为真或 $$xH$$ 为真。在第 1 种情况下，有 $$\exists x\ xS$$；在第 2 种情况下，有 $$\exists x\ xH$$。因此无论哪种情况，$$\exists x\ xS\lor xH$$ 在该情形都为真。

**第 4 章**：令

> $$xP$$ 为“$$x$$ 想获奖”
>
> $$xR$$ 为“$$x$$ 赢了比赛”

令考虑中的对象为所有人。推断符号化为：

$$
\dfrac{\forall x\ xP}{(\iota x\ xR)P}
$$

该推断是无效的。考虑某个情形 $$s$$，其中所有人都满足 $$P$$，但没有人满足 $$R$$。（也许比赛取消了！）那么前提在 $$s$$ 为真。但摹状词 $$\iota x\ xR$$ 不指称任何东西。因此，结论在 $$s$$ 为假。

**第 5 章**：令

> $$m$$ 为“你做了个煎蛋”
>
> $$b$$ 为“你打破了一个鸡蛋”

则推理符号化为：

$$
\dfrac{m\quad\neg(m\land\neg b)}{b}
$$

该推断是无效的。[^1] 考虑如下情形：

> $$b$$：$$F$$ 但不为 $$T$$
>
> $$m$$：$$T$$ 且 $$F$$

则 $$\neg b$$ 为 $$T$$（且不为 $$F$$）；因此 $$m\land \neg b$$ 为 $$T$$ 和 $$F$$（两个合取项均为真，且其中一个为假）；因此 $$\neg(m\land \neg b)$$ 为 $$T$$ 和 $$F$$。在该情形下，两个前提均为 $$T$$，而结论不为 $$T$$。

**第 6 章**：令

> $$f$$ 为“猪会飞”。
>
> $$b$$ 为“猪能在水下呼吸”。

则推断符号化为

$$
\dfrac{\neg\Diamond f\land\neg\Diamond b}{\Box(\neg f\land\neg b)}
$$

该推断是有效的。因为假设前提在某个情形 $$s$$ 为真，则两个合取项在该情形都为真。因此，没有关联情形 $$s'$$ 使得 $$f$$ 为真（第 1 个合取项）或 $$b$$ 为真（第 2 个合取项）。即，在每个关联情形 $$s'$$，$$\neg f\land\neg b$$ 均为真。因此，结论在 $$s$$ 为真。

**第 7 章**：令

> $$b$$ 为“你信仰上帝”
>
> $$c$$ 为“你去教堂”

则推断符号化为：

$$
\dfrac{b\to c\quad c}{b}
$$

该推断是无效的。[^2] 考虑某个情形 $$s$$，它有一个关联情形 $$s'$$，相关信息图示如下：

<div style="text-align: center">
<img src=/pics/situation4.png/>
</div>

在每个 $$b$$ 为真的情形，$$c$$ 都为真。因此，$$b\to c$$ 在 $$s$$ 为真。这样，两个前提在 $$s$$ 均为真，但结论在 $$s$$ 不为真。

**第 8 章**：令

> $$r$$ 为“现在在下雨”

则推断符号化为：

$$
\dfrac{\mathbf{H}r\land\mathbf{G}r}{r}
$$

该推断是无效的。考虑如下图示的情形组合：

| $$\ldots$$ | $$s_{-3}$$ | $$s_{-2}$$ | $$s_{-1}$$ |  $$s_0$$   | $$s_1$$ | $$s_2$$ | $$s_3$$ | $$\ldots$$ |
| :--------: | :--------: | :--------: | :--------: | :--------: | :-----: | :-----: | :-----: | :--------: |
|            |   $$r$$    |   $$r$$    |   $$r$$    | $$\neg r$$ |  $$r$$  |  $$r$$  |  $$r$$  |            |

$$r$$ 在 $$s_0$$ 之前的所有时刻均为真，故 $$\mathbf{H}r$$ 在 $$s_0$$ 为真。$$r$$ 在 $$s_0$$ 之后的所有时刻均为真，故 $$\mathbf{G}s$$ 在 $$s_0$$ 为真。因此，$$\mathbf{H}r\land\mathbf{G}s$$ 在 $$s_0$$ 为真。但结论在 $$s_0$$ 不为真。

**第 9 章**：令

> $$p$$ 为“帕特”
>
> $$c$$ 为“那个擦窗户的人”
>
> $$w$$ 为“是个女人”

则推断符号化为：

$$
\dfrac{pW\land\neg cW}{\neg p=c}
$$

该推断是有效的。考虑任何前提为真的情形，则在该情形下，$$p$$ 指称的任何对象都具有 $$W$$ 表达的性质，而 $$c$$ 指称的任何对象都不具有该性质。因此，据莱布尼茨律，$$p$$ 和 $$c$$ 指称不同的对象（假定没有什么可以既真又假！）。即，$$\neg p=c$$ 为真。

**第 10 章**：令

> $$c$$ 为“珍妮聪明”
>
> $$b$$ 为“珍妮漂亮”

则推断形式化为：

$$
\dfrac{c\quad \neg c\lor b}{b}
$$

该推断是无效的。[^3] 考虑某个 $$c$$ 和 $$b$$ 具有如下真值的情形：

> $$c$$：0.5
>
> $$b$$：0.2

则 $$\neg c$$ 的真值为 $$0.5$$（$$1-0.5$$），因而 $$\neg c\lor b$$ 的真值也为 $$0.5$$（$$\max(0.5,0.2)$$）。这样两个前提都是可接受的（$$\geq 0.5$$），但结论不是可接受的。

**第 11 章**：令

> $$t$$ 为“$$r$$ 高”
>
> $$w$$ 为“$$r$$ 富有”
>
> $$h$$ 为“$$r$$ 快乐”

推断是有效的。因为有 3 个高且富有的人，其中 2 个是快乐的，故 $$pr(h|t\land w)=2/3$$；其中 1 个是不快乐的，故 $$pr(\neg h|t\land w)=1/3$$。因此，$$pr(h|t\land w) > pr(\neg h|t\land w)$$。

**第 12 章**：第 1 问：考虑一个 100 人的具有该症状的典型样本，则 90 人得 $$A$$ 病，10 人得 $$B$$ 病。由于检查的正确率是 9/10，检查结果会告诉我们 90 个得 $$A$$ 病的人中有 81 个得 $$A$$ 病、9 人得 $$B$$ 病；10 个得 $$B$$ 病的人中有 $$9$$ 人得 $$B$$ 病、1 人得 $$A$$ 病。因此，总共有 18 人检查结果为 $$B$$ 病，因此一个随机抽中的人检查结果为 $$B$$ 病的概率为 18/100。

第 2 问：令 $$r$$ 为随机抽中的具有该症状的人，且令

> $$b$$ 为“$$r$$ 得 $$B$$ 病”
> $$t$$ 为“$$r$$ 的检查结果为 $$B$$ 病”

则：

- $$pr(t|b)=9/10$$，因为检查的正确率为 90%；
- $$pr(b)=1/10$$，因为 10 人中有 1 人得 $$B$$ 病；
- $$pr(t)=18/100$$，据第 1 问。

据互逆概率之间的关系可得，

$$
pr(b|t)=pr(t|b)\times pr(b)/pr(t)=\frac{9}{10}\times \frac{1}{10}\div\frac{18}{100}=1/2
$$

**第 13 章**：将相关信息用表格表示如下：

|      |           出事故            |          不出事故          |
| :--: | :----------------------: | :--------------------: |
| 买保险  | $$0.05\backslash -390$$  | $$0.95\backslash -90$$ |
| 不买保险 | $$0.05\backslash -1500$$ |  $$0.95\backslash 0$$  |

计算期望值可得：

$$
\begin{aligned}
E(t) &= 0.05\times(-390)+0.95\times(-90)=-105 \\
E(\neg t) & = 0.05\times(-1500)+0.95\times 0=-75
\end{aligned}
$$

由于 $$E(\neg t) > E(t)$$，因此你应该不买保险。

**第 14 章**：我们当然可以对给定的输入运行程序。如果它确实终止，则或早或晚它会终止，那时我们就知道它终止（尽管我们可能无法提前知道要多久它才会终止）。但是，如果它不终止，我们将永远无法知道这一点。无论计算持续了多长时间，如果它没停，这可能是因为它永远不会终止，但也可能只是它还没到终止的时候。我们没办法知道究竟处于哪种情形。

**第 15 章**：没有。如果 $$n$$ 是语句 $$\neg\exists xProv(x,n)$$ 的编码，则由于逻辑具有排中律，该理论能证明 $$\exists xProve(x,n)\lor\neg\exists xProv(x,n)$$。但哥德尔定理表明 $$\neg\exists xProv(x,n)$$ 无法被证明，尽管它是真的。

---

[^1]: 译者注：在经典逻辑中，该推断是有效的。因本章讨论的是有 4 个真值的逻辑，所以这里给出的答案是相反的。
[^2]: 译者注：事实上，该推断不仅在条件句逻辑中是无效的，在经典逻辑中也是无效的。

[^3]: 译者注：同样，该推断在经典逻辑中是有效的。因本章讨论的是模糊逻辑，所以这里给出的答案是相反的。