+++
author = "koji ota"
title = "my first content"
date = "2024-12-16"
description = "my first content"
tags = [
    "hugo",
]
math = true
+++


# h1
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

## h2
```scala
import com.databricks.connect.DatabricksSession
import org.apache.spark.sql.SparkSession

object Main {
  def main(args: Array[String]): Unit = {
    val spark = DatabricksSession.builder().getOrCreate()
    val df = spark.read.table("samples.nyctaxi.trips")
    df.limit(5).show()
  }
}
```

## h2


$y=3x$のように文章に数式を埋め込むことが出来ます。\\(y=3x\\)のような書き方にも対応しています。


Block math2:

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$


## ディスプレイ表示
中央に大きく表示されます。2通りの記述方法があります。Tabキーを使用すれば、一度に4つの空白を入力できます。
$$
x^n+y^n=z^n
$$

# 記述例
いくつかの記述例を紹介します。
## 四則演算
$$
    (-1)\times(-1)+1\div2-5=\,?
$$
## コメント
$$
    \overbrace{(-1)\times(-1)}^{\text{先に計算}}+\overbrace{1\div2}^{\text{先に計算}}-5=-\frac{7}{2}
$$
## 複数行にまたがる式
$$
\begin{aligned}
& (-1)\times(-1)+1\div2-5 \\\\ 
&= 1+0.5-5=-3.5
\end{aligned}
$$

## 連立方程式
$$
    \begin{cases}
    x+y &= 1 \\\\ 
    3x+2y & = 0\\
    \end{cases}
$$

## ベクトル
$$
	\bm{a},\bm{b},\bm{c} \\\\
	\vec{x},\vec{y},\vec{z}
$$

## 行列
$$
    \begin{pmatrix}
       a & b \\\\ 
       c & d
    \end{pmatrix}
    ^{-1}
    =
    \frac{1}{ad-bc}
    \begin{pmatrix}
       d & -b \\\\ 
       -c & a
    \end{pmatrix}
$$

## 論理式
$$
    (\forall \lambda \in \Lambda)[A_\lambda \neq \empty] \implies \prod_{\lambda \in 
    \Lambda} A_\lambda \neq \empty
$$
ギリシャ文字等の特殊文字や論理記号は、[こちら](https://katex.org/docs/supported.html#letters-and-unicode)と[こちら](https://katex.org/docs/supported.html#logic-and-set-theory)に表があります。

## 式番号
$$
    \tag{1} f(x)=\sin^2 x+1
$$

## 空白
$$
    \alpha \, \beta \: \gamma \; \delta
$$
詳しくは[こちら](https://katex.org/docs/supported.html#overlap-and-spacing)に表があります。

## 括弧
5つの大きさが用意されています。
$$
	(\big( \Big( \bigg( \Bigg(\Bigg) \bigg) \Big) \big) )
$$
以下の記法は、括弧の大きさを中身の大きさにある程度自動で合わせてくれます。
$$
	\left( \frac{b}{a} \right)
$$

<!-- # マクロ定義 -->
<!-- マクロを定義することで、煩雑な表現を簡潔に記述することが出来ます。面倒な場合は以下の例をコピペして使用してください。好きなようにカスタマイズすることも可能です。一度定義すれば、それより下のページ内ならば、どこからでも参照できます。 -->
<!-- ## 記号 -->
$$
    \gdef\abs#1{\left|#1\right|} 
    \gdef\norm#1{\left\|#1\right\|} 
    \gdef\tr{\mathrm{tr}\,} 
    \gdef\rank{\mathrm{rank}\,} 
    \gdef\re{\mathrm{Re}\,} 
    \gdef\im{\mathrm{Im}\,} 
    \gdef\Res{\mathrm{Res}\,} 
    \gdef\erf{\mathrm{erf}\,} 
$$
$$
    \abs{a}, \norm{b-a},\rank A, \tr \rho,
    \re Z,\im Z,\Res[f(z)],\erf(x)
$$

一度定義したので、$\tr \rho$のように、参照できます。
## 微分
$$
    \gdef\dd{\mathrm{d}}
    \gdef\d#1{\frac{\dd}{\dd #1}}
    \gdef\dv#1#2{\frac{\dd #2}{\dd #1}} 
    \gdef\ndv#1#2#3{\frac{\dd^{#3} #2}{\dd #1^{#3}}} 
$$

$$
    \dd x, \d{x}, \dv{x}{f}, \ndv{x}{f}{n}
$$

## 偏微分
$$
    \gdef\pd#1{\frac{\partial}{\partial #1}} 
    \gdef\pdv#1#2{\frac{\partial #2}{\partial #1}}
    \gdef\pndv#1#2#3{\frac{\partial^{#3} #2}{\partial #1^{#3}}} 
$$

$$
    \pd{x}, \pdv{x}{f}, \pndv{x}{f}{n}
$$

## ベクトル解析
$$
    \gdef\div{\nabla \cdot}
    \gdef\rot{\nabla \times}
    \gdef\laplacian{\nabla ^2}
$$

$$
	\div \vec{a}, \rot \vec{a}, \laplacian f
$$

## 物理数学
$$
    \gdef\bra#1{\left\lang#1\right|}
    \gdef\ket#1{\left|#1\right\rang} 
    \gdef\braket#1#2{\left\lang#1\middle|#2\right\rang} 
    \gdef\braopket#1#2#3{\lang#1|#2|#3\rang} 
    \gdef\comm#1#2{\left[#1,\,#2\right]} 
    \gdef\slash#1{{#1\!\!\!/}} 
$$

$$
    \bra{a}, \ket{b}, \braket{\phi}{\psi}, \braopket{a}{\hat{O}}{b} \\\\
    \comm{\hat{x}}{\hat{p}}, \\\\
    \slash{a}\slash{b}+\slash{b}\slash{a}
$$

<!--     \bra{a}, \ket{b}, \braket{\phi}{\psi}, \braopket{a}{\hat{O}}{b} \\ -->
<!--     \comm{\hat{x}}{\hat{p}}, \acomm{\hat{x}}{\hat{p}} \\ -->
<!--     \slash{a}\slash{b}+\slash{b}\slash{a} -->
