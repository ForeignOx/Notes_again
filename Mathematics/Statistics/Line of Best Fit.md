Linear line of best fit of the form: $y=a+bx$
We want this to be as close to as many points as possible by minimising vertical distance from the line. We want to make predictions (y value for a given x value) for interpolating and extrapolating.
## Residuals
![[Line of Best Fit 2024-02-26 11.00.56.excalidraw]]
Residuals are the vertical distance from the line
$$
\epsilon _{i}=y_{i}-\hat{y}_{i}
$$ Where $x_{i}, \hat{y}_{i}$ is the predicted value, so $\hat{y}_{i}=a+bx_{i}$
## Least Squares Regression Line of y on x
Least because we are minimising, squares as it is the residuals squared, regression line means line of best fit, y on x as we are predicting y from x
Minimise
$$
\sum_{i=1}^{n}\epsilon_{i}^{2}=\sum_{ i=1} ^{ n}(y_{i}-\hat{y_{i}})^{2}=\sum (y_{i}-(a+bx_{i}))^{2}
$$
Start by focusing on a choice of $a$
$$
\sum\epsilon_{i}^{2}=\sum((a+{bx_{i}})-y_{i})^{2}=\sum(a+(bx_{i}-y_{i}))^{2}
$$
$$
=\sum(a^{2}+2a(bx_{i}-y_{i})+(bx_{i}-y_{i})^{2})
$$
$$
=na^{2}+2a\sum(bx_{i}-y_{i})+\sum(bx_{i}-y_{i})^{2}
$$
$$
=n\left( a^{2}+\frac{2}{n}a\sum(bx_{i}-y_{i}) \right)+\sum(bx_{i}-y_{i})^{2}
$$
$$
=n\left( \left( a+\frac{1}{n}\sum(bx_{i}-y_{i}) \right)^{2}-\left( \frac{1}{n}\sum(bx_{i}-y_{i}) \right)^{2} \right)+\sum(bx_{i}-y_{i})^{2}
$$

We want the first bracket to be 0, so minimised when:
$$
a+\frac{1}{n}\sum(bx_{i}-y_{i})=0
$$
$$
\implies a+b \frac{\sum x_{i}}{n}-\frac{\sum y_{i}}{n}=0
$$
$$
\implies a+b\bar{x}-\bar{y}=0
$$
$$
\implies \bar{y}=a+b\bar{x}
$$
so $(\bar{x},\bar{y})$ is on the line
Next focus on choice of $b$
$$
\sum \epsilon_{i}^{2}=\sum(y_{i}-(a+bx_{i}))^{2}=\sum(bx_{i}+(a-y_{i}))^{2}
$$
$$
=\sum(b^{2}x_{i}^{2}+2bx_{i}(a-y_{i})+(a-y_{i})^{2})
$$
Take partial derivative with respect to $b$ to minimise
$$
\frac{ \partial  }{ \partial b } \sum\epsilon_{i}^{2} =2b\sum x_{i}^{2}+2\sum x_{i}(a-y_{i})
$$
At minimum point:
$$
2b\sum x_{i}^{2}+2\sum x_{i}(a-y_{i})=0
$$
Substitute $a$
$$
b\sum x_{i}^{2}+\sum (x_{i}(\bar{y}-b\bar{x}-y_{i}))=0
$$
$$
\implies b\sum x_{i}^{2}+\bar{y}\sum x_{i}-b\bar{x} \sum x_{i} -\sum x_{i}y_{i}=0
$$
$$
\implies b\left( \sum x_{i}^{2}-\bar{x}\sum x_{i} \right)=\sum x_{i}y_{i}-\bar{y}\sum x_{i}
$$
$$
\implies b S_{x x}=S_{xy}
$$
$$
\implies b=\frac{S_{x y}}{S_{x x}}
$$
So least squares regression line of y on x is $y-\bar{y}=b(x-\bar{x})$, where $b=\frac{S_{x y}}{S_{x x}}$
If you want the least squares regression line of x on y, it is $x-\bar{x}=b(y-\bar{y})$, where $b=\frac{S_{x y}}{S_{y y}}$
## Sum of residuals
Given that a regression line $a+bx$ goes through $(\bar{x},\bar{y})$, what can we say about the sum of residuals $\sum \epsilon_{i}$
$$
\sum \epsilon_{i}=\sum(y_{i}-\hat{y}_{i})=\sum(y_{i}-(a+bx_{i}))
$$
$$
=\sum y_{i} -na -b\sum x_{i} = n\bar{y}-na-bn\bar{x}
$$
$$
=n(\bar{y}-a-b\bar{x})
$$
Since $(\bar{x},\bar{y})$ is on the line $y=a+b\bar{x}$, $\bar{y}=a+b\bar{x}$, Hence
$$
\sum \epsilon_{i} = n(a+b\bar{x}-a-b\bar{x})=0
$$

#Mathematics #Statistics