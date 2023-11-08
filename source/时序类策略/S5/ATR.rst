.. vim: syntax=rst

ATR-RSI策略
=========

6.1计算方法
-------

ATR指标：ATR称为均幅指标，也称作平均真实波动或真实波动均值，是一种表示市场变化率的指标。

.. math::

   TR = max\left\{ \begin{array}{r} \ \ \ {High}_{T} - {Low}_{T}, \\ abs\left( {Close}_{T - 1} - {High}_{T} \right), \\ abs\left( {Close}_{T - 1} -
   {Low}_{T} \right)\ \end{array} \right\}

.. math:: ATR = SMA(TR,N)

RSI指标：

.. math:: RSI = \frac{upavg}{upavg + dnavg} \times 100

以表示市场一定时期的景气程度。它的范围在0到100之间，通常RSI处于30到70之间，在10到20之间时，市场处于超卖状态，后市将会出现价格反弹回升；在80到90之间，市场处于超买状态，后市将会出现价格回落。

6.2策略逻辑
-------

（1）设置参数：RSI的上轨\ :math:`self.rsi\_ buy` 下轨\ :math:`self.rsi\_ sell`

（2）空仓：如果当前ATR的值大于ATR的N日均值，并且RSI的值大于上轨则开多；如果当前ATR的值大于ATR的N日均值，并且RSI的值小于下轨时则开空；

（3）多头：(止盈价格)long_stop = intra_trade_high \* (1 - trailing_percent / 100)

（4）空头：(止盈价格)short_stop = intra_trade_low \* (1 + trailing_percent / 100)
