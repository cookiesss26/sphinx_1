.. vim: syntax=rst

AO策略
====

Awesome Oscillator (AO) 是一个动量指标，反映了市场驱动力的精确变化，有助于确定趋势的强度，直至形成和反转的点。

7.1 计算方法
--------

.. math:: Awesome\ Oscillator\  = \ SMA\ (MEDIAN\ PRICE,5\ PERIODS)–\ SMA\ (MEDIAN\ PRICE,\ 34\ PERIODS)

.. math:: MEDIAN\ PRICE = (\frac{{High}_{T} + {Low}_{T}}{2})

7.2 策略逻辑
--------

做多：\ :math:`Awesome\ Oscillator > 0`\ ；做空：\ :math:`Awesome\ Oscillator < 0`\ 。
