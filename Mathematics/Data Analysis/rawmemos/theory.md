#### Traditional methods

* ordinary/globalized/weighted/normalized least squares: min($[Y_{i}-(b_{i}x_{i}+b_{i+1}+e_{i})]^{2}$): $(A^{T} A)^{-1}(Y=AX)$

  * A: matrix of $x_{i}^{j}$, i: row j: col
  * X: col matrix of $a_{j}$
  * $A^{T}A=\sum_{i, j}(e_{ij}\sum_{k}^{m}x_{k}^{(i+j-2)})$ is always diag, A is unknown ($e_{ij}: \delta^{(rc), (ij)}$)
  * $\frac{\mathrm{d}\sum e_{i}^{2}}{\mathrm{d}b_{\alpha}}=-2\sum e_{i} \text{ or } -2\sum e_{i}x_{i}=0, \alpha=i \text{ or } j$: orthogonal equations(if AND)
  * $\sum e_{i}=\sum (Y_{i}-b_{i}-b_{i+1}x_{i})=0 = (\sum Y_{i} \rarr \bar{Y})-nb_{i}-b_{i+1}(\sum x_{i} \rarr \bar{X}) \rarr b_{i}=\bar{Y}-b_{i+1}\bar{X}$
  * $\sum x_{i}e_{i}=\sum x_{i}(Y_{i}-b_{i}-b{i+1}x_{i}) = 0 \text{ and above } \rightarrow b_{i+1}=\frac{\sum x_{i}(Y_{i}-\bar{Y})}{\sum (x_{i}-\bar{X})x_{i}}=\frac{S_{xy}}{S_{xx}}$
  * Gauss-Marcos Theorem: cond of Best Linear Unbiased Estimator=Minimum Variance Linear Unbiased Estimator
    * Linearity of $b_{i} \text{ or } \beta_{i}$
    * Nonstochasticity of $x_{i} or X$, not have probablities. cf) 2SLS
    * Identification: $S_{x}^{2}=\frac{1}{n-1}\sum (x_{i}-\bar{X}) \neq= 0$, at least 2 Y vars
    * avg(err)=0, err have no statistic meaning: +errs-errs$\rightarrow$ 0
    * Scedasticity: Homo | cf) hetero
      * $V(e_{i})=avg(e_{i}^{2})=\text{constant }\sigma^{2}$
    * AutoCorrelation: None about $e_{i}$s, they are independant | cf)auto/self
      * $Cov(e_{i}, e_{j})=avg((e_{i}-avg(e_{i})^{2}(e_{j}-avg(e_{j})^{2})=0$
    * called "Classical Regression Model" if all are satisfied. furthers: refer [this](https://namu.wiki/w/%EC%B5%9C%EC%86%8C%EC%A0%9C%EA%B3%B1%EB%B2%95)
* LASSO, Ridge....
* 2-StageLeastSquares(fixed effects, instrumental variables): Stochasticity case

  * set toolvar z: $\hat{x_{i}}=b_{0}+b_{z1}z+b_{xj}x_{j}+e_{j}$
  * replace $x_{i}$ to $\hat{x_{i}}$ and do OLS/GLS...
* Cointegration: nums of diffs to stationary, long-term relations between vars

  * vars' same coint order in all time
  * new time generated from linear comb. of prev times has lower order
  * prevent spurious correlation problem: from prev(remove trends and do LR)
* Granger causality: intervar causality in time. required cond. of actual causality not equal
* Generalized AutoRegressive Conditional Heteroskedasticity

  * GARCH(p, q): $\sigma_{t}^{2}=\sum (\alpha_{q}e_{t-q}^{2}+\beta_{p}\sigma_{t-p}^{2})$, ARCH: ave is also predictible case
  * related to Fourier transformation about $\sigma (f)=\int \sigma_{t}e^{2\pi ft}\mathrm{d}t$ (e: not ERR, exp)
* Generalized Methods of Momentum estimations

### Breaking cases of independant and identically distribution

#### Heteroskedasticity

do GLS, robust covariance matrix estimation

#### Endogeneity

related $x_{i}$ and $e_{i}|\epsilon_{i}$ by omitted vars(solve by Panal Analysis), simultaneity in time(solve by adding time-parallax vars), measure err

solve: adding control|investment vars, DiD model, etc

#### Multi-collinearity

remove/scalemod(log/diff....), Panel Analysis, ...

### Panel Analysis

* same time and attrition(null) t/f->balanced/unbalanced
  * can optimize unbalanced into small bias by Wooldridge Method (Akay, 2009)
* log scale or logistic to linearize skeweds/outliners in normalized view
* also analyze state dep(t-1 affect to t)

x, y, lagged(y)

#### Nonstational Panel Method

Solve falses by randomness in time dim->can use all data in all times to analysis with low false imaginations

##### Unit root tests: most pre-test

unit root exist: then NPM is valid

Augmented Dickey-Fuller, ADF-Fisher, Im, Pesaran and Shin's W-test, Levin, Lin and chu's t-ratio test, ...

##### Panel Cointegral

dynamic OLS(best in finite set), fully-modified OLS, CCR

#### Handling Err from t-indep, invisible omitted vars

Hausman test: $Cov(x_{it}, \mu_{i})$

##### =0: Fixed Effect Model

grad, bias are t-indep

###### cons

ignore effects from fixvars-descvars relations and lagged dependant vars. requires slices as varnums

##### $\neq 0$: Random Effect Model

###### Error Component Model

One Way: $u_{it}=\mu_{i}+\epsilon_{it}$, Two Way: $u_{it}=\mu_{i}+\epsilon_{it}+\lambda_{t}$ (additional: unobserved time effect)
