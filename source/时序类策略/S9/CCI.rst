.. vim: syntax=rst

CCI策略
=====

CCI指标是一种超买超卖指标。所谓超买超卖指标，顾名思义，"超买"，就是已经超出买方的能力，买进的人数超过了一定比例，那么，这时候应该反向卖出股票。"超卖"则代表卖方卖过了头，卖的人数超过一定比例时，反而应该买进。

8.1计算方法
-------

.. math::

   \begin{aligned} & CCI = \frac{TP - ATP}{0.015 \times MD} \\ & TP = \frac{high_{n} + low_{n} + close}{3} \end{aligned}

.. math:: ATP = \frac{\sum_{i = t - n + 1}^{i = t}{close}}{n}

.. math:: MD = \frac{\sum_{i = t - n + 1}^{i = t}{(ATP - close)}}{n}

设置参数n，\ :math:`high_{n}`\ 为n天内的最高价，\ :math:`low_{n}`\ 为n天内的最低价，\ :math:`ATP`\ 为\ :math:`TP`\ 的n日简单移动平均，\ :math:`MD`\ 为\ :math:`TP`\ 的N日平均绝对方差。

8.2策略逻辑
-------

做多：当CCI指标向上穿过100值，

做空：当CCI指标向下穿过-100值。
