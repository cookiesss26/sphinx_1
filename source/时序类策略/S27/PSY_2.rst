.. vim: syntax=rst

PSY策略
=====

PSY（Moving Average Convergence and Divergence）作为一种技术指标，主要反映了投资者对股市涨跌产生心理波动的情绪。

28.1计算方法
--------

.. math:: PSY\  = \frac{M(上涨天数)}{N(总天数)}*100

28.2策略逻辑
--------

做多：\ :math:`PSY < {PSY}_{low}`\ 处于超卖状态，对标的看多

做空：\ :math:`PSY > {PSY}_{high}`\ 处于超买状态，对标的看空

注：代码中取参数\ :math:`{PSY}_{high}`\ 为65，\ :math:`{PSY}_{low}`\ 为35
