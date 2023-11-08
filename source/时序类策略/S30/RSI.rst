.. vim: syntax=rst

RSI策略
=====

相对强弱指数（RSI）计算最近价格上涨与绝对价格上涨的比率。RSI在0到100之间

5.1 计算方法
--------

.. math::

   \left\{ \begin{array}{r} up = \text{ close }_{t} - \text{close }_{t - 1},dn = 0\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \text{close }_{t} > \text{close
   }_{t - 1} \\ dn = {\ close\ }_{t - 1} - \ {close\ }_{t}\ ,up = 0\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \text{ close }_{t} \leq \text{close }_{t - 1}
   \end{array} \right.\

.. math::

   \begin{aligned} & upavg = \frac{{upavg}_{n - 1} \times (n - 1) + up}{n} \\ & dnavg = \frac{{dnavg}_{n - 1} \times (n - 1) + dn}{n} \end{aligned}

.. math:: RSI = \frac{upavg}{upavg + dnavg} \times 100

5.2策略逻辑
-------

做多：当 RSI 小于买入阈值时，处于超卖，对标的看多；

做空：RSI 大于卖出阈值时，处于超买，对标的看空。
