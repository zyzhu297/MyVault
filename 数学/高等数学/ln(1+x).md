## $\ln(1+x)$ 常用不等式与证明方法

### 1. 常用不等式

对于 $x>0$：

$$
\boxed{
\frac{x}{1+x}<\ln(1+x)<x
}
$$

其中：

$$
\boxed{
\ln(1+x)>\frac{x}{1+x}
}
$$

以及：

$$
\boxed{
\ln(1+x)<x
}
$$

---

### 2. 证明 $\ln(1+x)>\dfrac{x}{1+x}$

令

$$
f(x)=\ln(1+x)-\frac{x}{1+x}.
$$

则

$$
f'(x)
=\frac{1}{1+x}-\frac{1}{(1+x)^2}
=\frac{x}{(1+x)^2}>0.
$$

所以 $f(x)$ 在 $x>0$ 上单调递增。

又因为

$$
f(0)=0,
$$

因此

$$
f(x)>0.
$$

即

$$
\boxed{
\ln(1+x)>\frac{x}{1+x}
}.
$$

> **方法：** 遇到这种 $\ln(1+x)$ 与有理式的比较，可以考虑构造差函数，然后利用单调性。

---

### 3. 证明 $\ln(1+x)<x$

令

$$
f(x)=x-\ln(1+x).
$$

则

$$
f'(x)
=1-\frac{1}{1+x}
=\frac{x}{1+x}>0.
$$

又

$$
f(0)=0.
$$

因此

$$
f(x)>0,
$$

即

$$
\boxed{
\ln(1+x)<x
}.
$$

---

## 4. 一个重要的积分恒等式

由

$$
\ln(1+x)=\int_0^x\frac{1}{1+t}\,dt
$$

可得

$$
\begin{aligned}
x-\ln(1+x)
&=\int_0^x1\,dt-\int_0^x\frac{1}{1+t}\,dt\\
&=\int_0^x\left(1-\frac{1}{1+t}\right)dt\\
&=\boxed{\int_0^x\frac{t}{1+t}\,dt}.
\end{aligned}
$$

这个形式在证明 $\ln(1+x)$ 的不等式时非常有用。

---

## 5. 利用积分证明更精细的不等式

对于 $x>0$，

$$
x-\ln(1+x)
=\int_0^x\frac{t}{1+t}\,dt.
$$

由于 $0\leq t\leq x$，有

$$
1+t\leq1+x,
$$

因此

$$
\frac{t}{1+t}\geq\frac{t}{1+x}.
$$

所以

$$
\begin{aligned}
x-\ln(1+x)
&\geq\int_0^x\frac{t}{1+x}\,dt\\
&=\frac{1}{1+x}\cdot\frac{x^2}{2}.
\end{aligned}
$$

即

$$
\boxed{
x-\ln(1+x)\geq\frac{x^2}{2(1+x)}
}.
$$

整理得

$$
\boxed{
\ln(1+x)
\leq
x-\frac{x^2}{2(1+x)}
}.
$$

---

## 6. 更常用的精细放缩

对于 $x>0$：

$$
\boxed{
x-\frac{x^2}{2}
<
\ln(1+x)
<
x-\frac{x^2}{2(1+x)}
}
$$

其中左边也可以通过积分证明：

$$
\ln(1+x)
=
x-\int_0^x\frac{t}{1+t}\,dt.
$$

由于

$$
\frac{t}{1+t}<t,
$$

所以

$$
\int_0^x\frac{t}{1+t}\,dt
<
\int_0^x t\,dt
=\frac{x^2}{2}.
$$

因此

$$
\ln(1+x)>x-\frac{x^2}{2}.
$$

---

## 7. 本题中的应用

题设：

$$
\ln(1+a_n)=\frac{a_n}{1+b_n},
\qquad
0<a_n<1,\quad 0<b_n<1.
$$

### （1）证明 $a_n>b_n$

由

$$
\ln(1+x)>\frac{x}{1+x}
$$

得

$$
\ln(1+a_n)>\frac{a_n}{1+a_n}.
$$

结合题设：

$$
\frac{a_n}{1+b_n}
>
\frac{a_n}{1+a_n}.
$$

由于 $a_n>0$：

$$
\frac{1}{1+b_n}
>
\frac{1}{1+a_n}.
$$

因此

$$
1+b_n<1+a_n,
$$

所以

$$
\boxed{a_n>b_n}.
$$

---

### （2）证明 $\displaystyle\sum(a_n-b_n)$ 收敛

因为

$$
\sum_{n=1}^{\infty}b_n
$$

收敛，所以

$$
\boxed{b_n\to0}.
$$

由

$$
\ln(1+x)
\leq
x-\frac{x^2}{2(1+x)}
$$

得

$$
\frac{a_n}{1+b_n}
\leq
a_n-\frac{a_n^2}{2(1+a_n)}.
$$

两边除以 $a_n>0$：

$$
\frac{1}{1+b_n}
\leq
1-\frac{a_n}{2(1+a_n)}.
$$

整理：

$$
\frac{b_n}{1+b_n}
\geq
\frac{a_n}{2(1+a_n)}.
$$

所以

$$
2b_n(1+a_n)\geq a_n(1+b_n),
$$

即

$$
2b_n\geq a_n(1-b_n).
$$

因此

$$
\boxed{
a_n\leq\frac{2b_n}{1-b_n}
}.
$$

由于 $b_n\to0$，所以存在 $N$，使得 $n>N$ 时

$$
b_n<\frac12.
$$

于是

$$
a_n
\leq\frac{2b_n}{1-b_n}
<4b_n.
$$

结合 $a_n>b_n$：

$$
0<a_n-b_n<a_n<4b_n.
$$

又因为

$$
\sum b_n
$$

收敛，根据比较判别法：

$$
\boxed{
\sum_{n=1}^{\infty}(a_n-b_n)
\text{ 收敛}
}.
$$

---

## 8. 解题思路总结

看到 $\ln(1+x)$，可以考虑的工具

**① 单调性**

构造差函数：

$$
f(x)=\text{左边}-\text{右边}
$$

然后通过 $f'(x)$ 判断大小。

---

**② 积分**

利用：

$$
\boxed{
\ln(1+x)=\int_0^x\frac{1}{1+t}\,dt
}
$$

特别是：

$$
\boxed{
x-\ln(1+x)
=
\int_0^x\frac{t}{1+t}\,dt
}
$$

将函数比较转化为**被积函数逐点比较**。

---

**③ 泰勒展开**

$$
\boxed{
\ln(1+x)
=x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\cdots
}
$$

适用于需要比较高阶无穷小或求极限的情况。

---

**④ 拉格朗日中值定理**

对于

$$
\ln(1+x)-\ln1
$$

可以写成

$$
\ln(1+x)=\frac{x}{1+\theta x},
\qquad 0<\theta<1.
$$

有时可以用于建立上下界。