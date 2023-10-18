#  机器学习

## 有监督的机器学习

### define

given right answer for each in example in the data	reg/classifition

对无穷多的特征作预测

### cost function

代价函数

training set 训练样本

m 样本量	x 输入变量	y 输出变量	x(i) i指第几行

**stuation1** : set parameters θ_0 = 0

![1697026945686](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697026945686.png)

h(x): hypothesus function

 J(θ_1): cost function

diference : h - x ; j - θ_1

relate :  J(θ_1) 是 假设函数拟合值与输出值差的平方和 / （2*样本数）

goal : minimize  J(θ_1)

![1697027207183](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697027207183.png)

**stuation2** : keep θ_1 and θ_0

only θ1: u 形

 θ1 and θ0 : 3D u 形

![1697027979560](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697027979560.png)

contour plots / contour figures （等高图）

![1697028234761](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697028234761.png)

### gradient descent

梯度下降

**use gradient descent to minimize functions**

have some function J( θ_1, θ_0 )

want min J( θ_1, θ_0 )

outline: keep changing θ_1, θ_0  to reduce J( θ_1, θ_0 ) until end up at minimum

![1697029472170](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697029472170.png)

if we started a different point, it will be a different local optimum

![1697029602596](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697029602596.png)

( := assignment ; = truth assetion ; convergence 收敛)

α : learning rate, controls how big step we take downhill whit gradient descent

large α means aggressive gradient descent procedure

（把cost function看作山，gradient descent就是寻找最快下山的路，α 就是下山的步伐。cost function有不同的区域最低点，不同起始点最终会到达不同的区域最低点。）

越接近局部最优解，∂/∂θ_j越小，会导致降低的数值越小，所以不需要更新α值。

### gradient descent for linear regresssion

梯度下降的线性回归

combine gradient descent with cost function

cost function for linear regression: convex function (so one global optimum) 

#### batch gradient descent

批量梯度下降

each step of gradient descent uses all the training examples

与之相对的是随机梯度下降

#### multiple features ( variables) 

多特征量

![1697201333627](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697201333627.png)

n: number of features 

m: number of variables

xj: feature j

x^(i): i^th features ( 第i行特征向量，也就是i样本的各个变量值组成的向量)

#### gradient descent for linear regression with multiple features

![1697202627182](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697202627182.png)

parameter : 参数

think of the parameters as θ where θ here is a n+1-dimensional vector

![1697203052762](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697203052762.png)

![1697203314218](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697203314218.png)

#### feature scaling 

特征缩放

make sure features are on similar scale (similar ranges of values), then gradient descence can converge more qiuckly

if the range of x1 is much larger than x2 it will be:

![1697203705961](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697203705961.png)

, it will be harder to find the global optimum

make features   -1 <=  x <= 1

#### learning rate *α* 

##### make sure gradient descent is working correctly

###### figure

![1697204302366](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697204302366.png)

if α too large: 

![1697204739839](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697204739839.png)

if α too small: slow

usually: samll to large; 0.001, 0.003, 0.01, 0.03, 0.1, 0.3....

and find [min_α, max_α], finally use a number which is close to max_α

###### automatic convergence test 

an example ( but it's difficult to for the threshold)

![1697204355468](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697204355468.png)

#### features and polynomial regression

特征值和多项式回归

##### a choice of features that you have

h_θ(x) = θ_0 + θ_1 * frontage + θ_2 * depth

h_θ(x) = θ_0 + θ_1*x (x = frontage * depth)

##### polynomial regression

多项式回归

h_θ(x) = θ_0 + θ_1*x + θ_2*x^2

#### normal equation

正规方程

for some linear regression problems,it will give us a much better way to solve for optimal value of the parameters 

one step to find the optimal value for θ (gradient dscent : many steps)

∂/∂θ  J(θ) = ... = 0

![1697274804895](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697274804895.png)

this is the value of θ that minimize cost function

normal equation don't need feature scaling

![1697275456138](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697275456138.png)

n >> 10^4 , cansider other method

##### normal equation and non-invertibility

正规方程及不可逆性

![1697365326017](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1697365326017.png)

X^T X矩阵不可逆：

1.redundant features(多余的特征) e.g.特征变量自相关

2.m<=n（delete some features or use regularization）







## 无监督的机器学习

### define

not given right answer	cluster（聚类）/鸡尾酒会算法

eg1 google对于新闻分类；一堆DNA组 判定基因表达程度

eg2 鸡尾酒会算法：从噪杂的声音中剥离出某种音源



octave编程环境

