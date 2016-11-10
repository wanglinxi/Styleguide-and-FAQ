
[<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/banner.png" alt="Visit QuantNet">](http://quantlet.de/index.php?p=info)

## [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/qloqo.png" alt="Visit QuantNet">](http://quantlet.de/) **Topic Modeling** [<img src="https://github.com/QuantLet/Styleguide-and-Validation-procedure/blob/master/pictures/QN2.png" width="60" alt="Visit QuantNet 2.0">](http://quantlet.de/d3/ia)

```yaml

Name of Quantlet: Topic Modeling

Published in: An Introduction of Topic Modeling. 

Description: Plots of Dirichlet distribution.

Keywords: Dirichlet, distribution, density plots.

Author: Linxi Wang
```

![Picture1](TM-1_1_m.png)
![Picture2](TM-1_2_m.png)
![Picture3](TM-1_3_m.png)
![Picture4](TM-1_4_m.png)

```r

function r = drchrnd(a,n)
p = length(a);
r = gamrnd(repmat(a,n,1),1,n,p);
r = r ./ repmat(sum(r,2),1,p);

a = [1 1 1];
n = 1000;
r = drchrnd(a,n);

HD=scatter3(r(:,1),r(:,2),r(:,3),'MarkerFaceColor',[1 0 0]);
direction = [1 0 0];
rotate(HD,direction,50)

```
