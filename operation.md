# basic operation

`help conmand`

打印变量：

```octave
>> disp(a)
```

maritx:

2*2 matrix

```
>> A =[ 12  23;34  45]
A =

   12   23
   34   45
```

1*3 matrix

```
>> a = [2 3 4]
a =

   2   3   4
```

```
>> b = [1;2;3]
b =

   1
   2
   3
```

[a: m: ​b] [起始值：步长：种植值]的行向量

```
>> v = [1:0.2:3]
v =

   1.0000   1.2000   1.4000   1.6000   1.8000   2.0000   2.2000   2.4000   2.6000   2.8000   3.0000
```

单位矩阵

```
>> B = ones(2,3)
B =

   1   1   1
   1   1   1
```

```
>> C = 3* ones(2,4)
C =

   3   3   3   3
   3   3   3   3
```

```
>> D= zeros(1,2)
D =

   0   0
```

random matrix

```
>> rand(3)
ans =

   0.8973   0.3855   0.6476
   0.1129   0.8015   0.6364
   0.3733   0.2083   0.1208
```

random matrix which drawn for Gaussian distribution

```
>> randn(1,3)
ans =

   0.9580   0.7884   1.0661
```

identity matrix

```
>> eye(4)
ans =

Diagonal Matrix

   1   0   0   0
   0   1   0   0
   0   0   1   0
   0   0   0   1
```

返回矩阵大小

```
>> size(A)
ans =

   2   2
```

返回A矩阵第一维度的大小（此处为行数）

```
>> size (A,1)
ans = 2
```

# moving data around

显示当前路径

```
>> pwd
ans = C:\Users\Administrator
```

change directory

```
>> cd 'D:\llin\py\machine_learning'
```

显示当前路径下的文件

```
>> ls
```

载入文件

```
>> load filename
```

```
>> load ('filename')
```

 who: the variables that octave has in memory

```
>> who
Variables visible from the current scope:

A    B    D    a    ans  b    c    v    w
```

whos: detailed view

```
>> whos
Variables visible from the current scope:

variables in scope: top scope

  Attr   Name        Size                     Bytes  Class
  ====   ====        ====                     =====  =====
         A           2x2                         32  double
         B           2x3                         48  double
         D           1x2                         16  double
         a           1x3                         24  double
         ans         1x22                        22  char
         b           3x1                         24  double
         c           2x4                         64  double
         v           1x11                        88  double
         w           1x100                      800  double

Total is 159 elements using 1118 bytes
```

delete variabal

```
clear variabal_name
clear #delete all variabals
```

save

```
save filename variable_name
```

: means every element along that row or column

```
>> B(2,:)
ans =

   1   1   1
```

```
>> B(:)
ans =

   1
   1
   1
   1
   1
   1

>> B(:,:)
ans =

   1   1   1
   1   1   1
```

为矩阵增加列/行

```
>> B
B =

   1   1   1
   1   1   1

>> B = [ B [3;3]]
B =

   1   1   1   3
   1   1   1   3

>> B= [B ;[4 4 4 4]]
B =

   1   1   1   3
   1   1   1   3
   4   4   4   4
```

```
>> B = rand (2,3)
B =

   0.028638   0.374084   0.836787
   0.645942   0.344218   0.934850

>> C = rand (2,1)
C =

   0.7814
   0.7093

>> BC= [B C]
BC =

   0.028638   0.374084   0.836787   0.781395
   0.645942   0.344218   0.934850   0.709318
```



