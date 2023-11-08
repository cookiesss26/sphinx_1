.. vim: syntax=rst

Adosc策略
=======

Chaikin A/D Oscillator Chaikin震荡指标：将资金流动情况与价格行为相对比，检测市场中资金流入和流出的情况。

2.1计算方法
-------

.. math:: {AD}_{t} = {AD}_{t - 1} + \text{ volume }_{t}\frac{\left( \text{close}_{t} - \text{low}_{t} \right) - \left( \text{high}_{t} - \text{close}_{t} \right)}{\left( \text{high}_{t} - \text{low}_{t} \right)}

若\ :math:`\text{ high }_{t} = \text{ low }_{t}`\ ，则

.. math:: {AD}_{t} = \frac{{\ close}_{t}}{\text{close}_{t - 1}} - 1

.. math:: ADOSC = {AD}_{fastperiod} - {AD}_{slowperiod}

其中，\ :math:`\text{ volume }_{t}`\ 为成交量；\ :math:`{AD}_{fastperiod}`\ 为AD的快速移动平均，参数\ :math:`fastperiod`\ 为 AD的快速移动平均窗口期，\ :math:`{AD}_{fastperiod}`\
为AD的慢速移动平均，参数\ :math:`slowperiod`\ 为AD的慢速移动平均窗口。

2.2策略逻辑
-------

做多：\ :math:`ADOSC`\ 由负变正；

做空：\ :math:`ADOSC`\ 由正变负。
