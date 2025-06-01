# Regression Analysis

from Francis Galton

## Linear Regression

"Regression" for AVG by Law of Large Numbers($\neq$Central Limit Theorem: $\lim_{n\rightarrow\infty}$child: randpick(mother) becomes normal distribut.)

### Bases

#### LLNums

Weak: $\lim_{n\rightarrow\infty} P(\frac{1}{n}\sum_{k-1}^{n}(x_{k}-\bar{X} < \epsilon)) = 1$, Strong: $P(\lim_{n\rightarrow\infty}\frac{1}{n}\sum_{k-1}^{n}x_{k}=\bar{X})=1$

#### Correlation Coefficient

##### "Co"variance

Variance($=\frac{\sum_{i}^{n}(x_{i}-\bar{X})^{2}}{n-1}=AVE((x-\bar{X})^{2})=AVE(x^{2})-{\bar{X}}^{2}$) between (normal.distrib.) vars

$Cov(x, y)=AVG((x-E_{x})(y-E_{y}))=\frac{\sum_{i}^{n}(x-E_{x})(y-E_{y})}{n-1}=E(xy)-E(x)E(y)-E(x)E(y)+E(x)E(y)=E(xy)-E(x)E(y), E(x) \equiv \bar{X} \equiv AVG(x)$

##### Pearson's r

Based on Cauchy-Schwarz-Bunyakovsky inequality, $norm(\nu)^{2}norm(\omega)^{2} \geq abs(\nu\dot\omega)^{2}$: about sum/integral/AVG...., related to the Uncirtainty on complex

$-1\leq r \leq 1=\frac{\sum_{i-1}^{n}z_{x}z_{y}}{n-1}=\frac{\sum_{i-1}^{n}x_{i}y_{i}-\frac{\sum_{i-1}^{n}x_{i}\sum_{i-1}^{n}y_{i}}{n}}{\sqrt{(\sum_{i-1}^{n}x_{i}^{2}-\frac{(\sum_{i-1}^{n}x_{i})^{2})^{2}}{n})(\sum_{i-1}^{n}x_{i}^{2}-\frac{(\sum_{i-1}^{n}x_{i})^{2})^{2}}{n})}} = \frac{Cov(x, y)}{\sigma^{x}\sigma^{y}}$, z: z-score

###### Coefficient of Determination

$R_{LSM}^{2}=\frac{\sum_{i}^{n}(y_{i}-\hat{y_{i}})^{2}\sum_{i}^{n}(y_{i}-\bar{y_{i}})^{2}}{(\sum_{i}^{n}(y_{i}-\bar{y_{i}})^{2})^{2}}=1-\frac{\sum_{i}^{n}(\epsilon_{i}-\hat{\epsilon_{i}})^{2}}{\sum_{i}^{n}(y_{i}-\bar{y_{i}})^{2}}$: rate of relation =$\frac{SqSum_{reg}}{SqSum_{tot}(y_{i}-\bar{y})}=\frac{(\sum_{i}^{n}(y_{i}-\bar{y})^{2})^{2}}{\sum_{i}^{n}(y_{i}-\bar{y})^{2}}, SqS_{tot}=SqS_{res}+SqS_{reg} \geq 0$ by Least Square Method condition

###### adjusted $R^{2}$

###### predicted $R^{2}$

###### t-score=$\frac{r}{\sqrt{\frac{1-r^{2}}{n-2}}}$

##### Spearman

##### Cronbach's $\alpha$

##### Akaike Information Criterion

##### Bayes Info Crite.

#### ERR

Type 1: ghost relations, Type 2: realtions lost

### Simple

### Multiple