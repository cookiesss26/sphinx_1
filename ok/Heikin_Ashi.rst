.. vim: syntax=rst

Heikin Ashi策略
=============

20.1计算方法
--------

.. math:: HA_{close} = \frac{(open\  + \ high\  + \ low\  + \ close)}{4}

.. math:: HA_{open} = \frac{\left( HA_{open}\  + HA_{close} \right)}{2}

.. math:: HA_{high} = max(high,HA_{open},HA_{close})

.. math:: HA_{low} = min(low,HA_{open},HA_{close})

（第一个\ :math:`HA_{open}`\ 取\ :math:`open`\ ）

20.2策略逻辑
--------

做多：

第t天与第t-1天：\ :math:`HA_{open} > HA_{close}`

且第t天\ :math:`HA_{open} = HA_{high}`

且第t天的\ :math:`\left| HA_{open} - HA_{close} \right|`\ 大于第t-1天的\ :math:`\left| HA_{open} - HA_{close} \right|`

做空：

第t天：\ :math:`HA_{open} < HA_{close}`\ 且\ :math:`HA_{open} = HA_{low}`\ 且第t-1天\ :math:`HA_{open} < HA_{close}`
