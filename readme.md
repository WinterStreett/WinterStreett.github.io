### 用途
描述两个随机变量之间的联系（线性相关）的数字特征，如果我们可以判定分布未知的随机变量和我们已经清楚掌握的随机变量之间有很强的随机关系，那么用已知的随机变量帮助我们研究未知的随机变量就有了依据。

---
### 协方差

```math
Cov(X,Y)=E{[X-E(X)][Y-E(Y)]}
```
#### 计算协方差的一个简单的公式

```math
Cov(X,Y)=E(X,Y)-E(X)E(Y)
```
从上面的公式进行定量的分析：
- 如果X和Y相互独立，那么E(X,Y)=E(X)E(Y),则Cov(X,Y)=0
- 如果X和Y相同，那么Cov(X,X)=D(X)

可以看出，协方差是和随机变量之间的相关程度成正比的，相互独立意味着没关系，这是协方差就是0；如果相同，就是强相关，协方差此时就是方差。

#### 方差和协方差的关系
D(X+Y)=D(X)+D(Y)+2Cov(X,Y)

---
### 相关系数
协方差虽然在一定程度上反映了随机变量之间的相关程度，但是会受到随机变量量纲的影响，为了克服这一缺点，提出相关系数。


```math
\rho_{XY} = \frac{Cov(X,Y)}{\sqrt{D(X)D(Y)}}
```
- 显然，相关系数的绝对值的取值范围是0~1，这是因为消除了量纲带来的数值影响
- 若X和Y独立，则相关系数为0，反之不成立，相关系数为0，只能说明X和Y不存在线性关系，但是可能存在其他关系
> 独立意味着两个变量之间没有任何关系，包括线性关系等；总之，相互独立是不相关的充分不必要条件（这个结论对于服从二维正态分布的随机变量不适用），以下四个式子是等价的：

```math
\rho_{XY}=0

Cov(X,Y)=0

E(X,Y)=E(X)E(Y)

D(X \pm Y)=D(X)+D(Y)
```
- 相关系数小于0时，表示随机变量之间是负相关，反之为正相关
- `$|\rho|=1$`表明存在常数a和b，使得`$P{Y=a+bX}=1$`