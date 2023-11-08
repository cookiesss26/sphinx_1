.. vim: syntax=rst

Heikin Ashi Simple 策略
=====================

19.1计算方法
--------

.. math:: HA_{close} = \frac{(open\  + \ high\  + \ low\  + \ close)}{4}

.. math:: HA_{open} = \frac{\left( HA_{open}\  + HA_{close} \right)}{2}

.. math:: HA_{high} = max(high,HA_{open},HA_{close})

.. math:: HA_{low} = min(low,HA_{open},HA_{close})

（第一个\ :math:`HA_{open}`\ 取\ :math:`open`\ ）

19.2策略逻辑
--------

做多：\ :math:`HA_{close}`\ 线上穿\ :math:`HA_{open}`\ 线

做空：\ :math:`HA_{close}`\ 线下穿\ :math:`HA_{open}`\ 线
