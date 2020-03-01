记对象 $i$ 的健康水平为 $Y_i$, 为了研究 $Y_i$ 是否受到医疗的影响, 考虑一个人的潜在健康水平, 潜在表明无论他是否接受了医疗, 这都是客观存在的随机变量.
$$
潜在健康水平=\left\{
\begin{array}{l}
Y_{1i} & if\ \mathbb{I}=1\\
Y_{0i} & if\ \mathbb{I}=0
\end{array}

\right.
$$
其中 $\mathbb I$ 为接受治疗的示性函数.

那么有
$$
Y_i=\left\{
\begin{array}{l}
Y_{1i} & if\ \mathbb{I}=1\\
Y_{0i} & if\ \mathbb{I}=0
\end{array}

\right.
$$
所以 
$$
Y_i=Y_{0i}+\mathbb I(Y_{1i}-Y_{0i})
$$
为了分析接受治疗带来的健康差异:
$$
\begin{align*}
E[Y_i|\mathbb I=1]-E[Y_i|\mathbb I=0]&=E[Y_{0i}+\mathbb I(Y_{1i}-Y_{0i})|\mathbb I=1]-E[Y_{0i}+\mathbb I(Y_{1i}-Y_{0i})|\mathbb I=0]\\
&=E[Y_{0i}|\mathbb I=1]+E[Y_{1i}-Y_{0i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=0]\\
&=E[Y_{1i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=1]+E[Y_{0i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=0]
\end{align*}
$$
其中 $E[Y_{1i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=1]=E[Y_{1i}-Y_{0i}|\mathbb I=1]$ 表示的是接受医疗的人接受的医疗的平均效应.

而 $E[Y_{0i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=0]$ 表示的是接受医疗的人和未接受治疗的人的原始健康水平差异, 因为他的结果反向于我们要研究的差异(因为需要接受医疗的人健康水平应该较差), 所以它被称为 **选择性偏误(selection bias)**.

如果我们能随机指定一个人是否接受医疗, 即使得 $\mathbb I$ 独立于 $Y_{0i}$ 和 $Y_{1i}$, 则 
$$
E[Y_{0i}|\mathbb I=1]=E[Y_{0i}|\mathbb I=0]
$$
这意味这我们可以消除选择性偏误, 同时有
$$
E[Y_{1i}|\mathbb I=1]-E[Y_{0i}|\mathbb I=1]=E[Y_{1i}-Y_{0i}|\mathbb I=1]=E[Y_{1i}-Y_{0i}]
$$
