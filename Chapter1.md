# 回归分析———引论
## 线性回归模型
1. 假设响应变量$ Y $ 与$ p-1 $ 个解释变量$ X_1,\dots,X_{p-1} $ 间有如下关系：
$$ Y = E(Y|X_1=x_1, \dots, X_{p-1}=x_{p-1}) + e
$$ 其中$ E(Y|X_1=x_1, \dots, X_{p-1}=x_{p-1}) $ 为理论均值函数。$ e $ 为随机误差，满足
    - $ E(e)=0 $ ;
    - $ Var(e)=\sigma^2 $ ;
    - 不同次观测的随机误差独立.
 
2. 对于线性回归有
$$ E(Y|X_1=x_1, \dots, X_{p-1}=x_{p-1})
=
\sum_{j=1}^{k} \beta_j f_j(x_1,\dots,x_{p-1})
$$ 其中$ f_1,\dots,f_k $ 为一组线性独立的已知函数.

3. 主要问题：参数估计、假设检验等；
4. 假设对$ Y,X_1,\dots,X_p $ 进行了$ n $ 次观察，得到观察值：
$$ \{(y_i, x_1, \dots, x_p), i=1,2,\cdots,n\}
$$ 满足关系式：
$$
y_i = \sum_{j=1}^{k} \beta_j f_j(x_{i_1},\dots, x_{i, p-1}) + e_i
$$ 引入矩阵记号，
$$
\boldsymbol{y} = (y_1, \dots, y_n)^T
$$ $$
\boldsymbol{X} = 
    \begin{pmatrix}
        f_{11}&\dots&f_{1k}\\
        \vdots &  & \vdots \\
        f_{n_1} & \dots & f_{nk}\\
    \end{pmatrix}
$$ $$
\boldsymbol{\beta} = (\beta_1, \dots, \beta_k)^T
$$ $$
\boldsymbol{e} = (e_1, \dots, e_n)^T
$$，
改写为矩阵形式：
$$
\boldsymbol{Y} = \boldsymbol{X} \boldsymbol{\beta} + \boldsymbol{e} 
$$
5. Gauss-Markov假设
   -  $ \mathbb{E}(e_i) = 0 $ ;
   -  $ Var(e_i) = \sigma^2 $ ;
   -  $ Cov(e_i, e_j) = 0,\ i\neq j $ ; 

