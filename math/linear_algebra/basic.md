Added: 18/05/03

---

# 1. Scalars 标量
A single number. lowercase italic

example:

$$
\textit{a}
$$

$$
\textit{b} \in ℝ
$$

# 2. Vectors 向量

## Definition

A vector is an array of numbers.

Represented by a lowercased bold typeface, for example:

$$
\textbf{a}
$$

>If each element of vector is in ℝ, and the vector has *n* elemens, then the vector lies in the set formed by taking the Cartesian product of ℝ n times.

## 表示形式

$$
\textbf{b} = \begin{Bmatrix} b_1 \\ b_2 \\b_3 \\...\\b_n \end{Bmatrix}
$$

## 向量子集

例如，要表示第3，4，6个向量元素，可以先定义一个元素索引值的集合 $\textit{S} = \lbrace{3,4,6 \rbrace}$, 然后用：

$$
\textbf{b}_S
$$

来表示所需表示的向量子集。并可在索引集合前添加负号，来表示除这几个索引值以外的向量集合：

$$
\textbf{b}_{-S}
$$


# 3. Matrix 矩阵

矩阵是一个2维数字的集合。通常使用大写粗体字符表示举证，例如：**A**
如果**A**的每个元素都是实数，并且有m行n列，则可以表示为$\textbf{A}\in ℝ^{m \times n} $

# 矩阵的表示方法

$$
\textbf{A} = \begin{bmatrix} A_{1,1} & A_{1,2} & A_{1,3} \\ A_{2,1} & A_{2,2} & A_{2,3}\end{bmatrix}
$$

## 矩阵中元素的表示方法

通常用大写字母（非粗体）加上下标来表示矩阵中的元素，元素的标示使用逗号分隔。例如：
$$
A_{m,n}
$$
代表矩阵$\textbf{A}$中的第$m$行,$n$列的元素。

## 表示矩阵整行或整列

使用“：”符号来表示矩阵整行或整列。例如，使用$\textbf{A}_{i,:}$来表示该矩阵的第i行，或使用$\textbf{A}_{:,i}$来表示矩阵的第i列

# 4. 张量 Tensors

张量即为超过二维的矩阵。张量用这种字体表示$\bf{\sf{A}}$

