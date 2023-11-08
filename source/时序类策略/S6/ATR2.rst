.. vim: syntax=rst

ATR策略
=====

ATR策略是一种基于波动率的交易策略，它使用平均真实范围（Average True Range，简称ATR）指标来确定股票等交易品种的价格波动区间，并根据这个波动区间制定交易策略。

4.1计算方法
-------

ATR指标：ATR称为均幅指标，也称作平均真实波动或真实波动均值，是用来衡量价格波动性的指标，它考虑了最高价、最低价和收盘价之间的差异。

.. math::

   TR = max\left\{ \begin{array}{r} \ \ \ {High}_{T} - {Low}_{T}, \\ abs\left( {Close}_{T - 1} - {High}_{T} \right), \\ abs\left( {Close}_{T - 1} -
   {Low}_{T} \right)\ \end{array} \right\}

.. math:: ATR = SMA(TR,N)

.. math:: 上轨 = {Close}_{T - 1} + ATR

.. math:: 下轨 = {Close}_{T - 1} - ATR

4.2策略逻辑：
--------

做多：当今日最高价突破前一日上轨

做空：当今日最高价跌破前一日下轨
