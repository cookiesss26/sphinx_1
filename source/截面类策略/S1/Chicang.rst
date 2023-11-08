.. vim: syntax=rst

持仓因子
====

3.1净多头持仓变化率
-----------

.. math:: \frac{(\text{ 多头持仓量 } - \text{ 空头持仓量 })_{t}}{(\text{ 多头持仓量 } - \text{ 空头持仓量 })_{t - R}} - 1

3.2净多头持仓量相对总持仓量占比变化率
--------------------

.. math:: \frac{(\text{ 多头持仓量 } - \text{ 空头持仓量 })_{t}}{\text{  }\text{总持仓量}_{t}\text{ }} - \frac{(\text{ 多头持仓量 } - \text{ 空头持仓量 })_{t - R}}{\text{ }\text{总持仓量}_{t - R}\text{ }}

3.3当前净多头持仓量占比
-------------

.. math:: \frac{(\text{ 多头持仓量 } - \text{ 空头持仓量 })_{t}}{(\text{ 多头持仓量 } + \text{ 空头持仓量 })_{t}}

3.4多头持仓量变化率
-----------

.. math:: \frac{\text{ 多头持仓量 }_{t}}{\text{  }\text{多头持仓量}_{t - R}} - 1

3.5空头持仓量变化率
-----------

.. math:: - (\frac{{\text{ }\text{空}\text{头持仓量 }}_{t}}{\text{  }{\text{空}\text{头持仓量}}_{t - R}} - 1)

3.6多头持仓量相对总持仓量占比变化
------------------

.. math:: \frac{\text{ 多头持仓量 }_{t}}{\text{ 总持仓量 }_{t}} - \frac{\text{ 多头持仓量 }_{t - R}}{\text{ 总持仓量 }_{t - R}}

3.7空头相对总持仓占比变化
--------------

.. math:: - (\frac{{\text{ }\text{空}\text{头持仓量 }}_{t}}{\text{ 总持仓量 }_{t}} - \frac{{\text{ }\text{空}\text{头持仓量 }}_{t - R}}{\text{ 总持仓量 }_{t - R}})

3.8多头与空头持仓变化方向
--------------

.. math:: sign\left( \frac{\text{ 多头持仓量 }_{t}}{\text{ 多头持仓量 }_{t - R}} - 1 \right) + sign\left( \frac{\text{ 空头持仓量 }_{t - R}}{\text{ 空头持仓量 }_{t}} - 1 \right)

3.9多头持仓变化方向
-----------

.. math:: sign\left( \frac{\text{ 多头持仓量 }_{t}}{\text{ 多头持仓量 }_{t - R}} - 1 \right)

3.10空头持仓变化方向
------------

.. math:: sign\left( \frac{\text{ 空头持仓量 }_{t - R}}{\text{ 空头持仓量 }_{t}} - 1 \right)
