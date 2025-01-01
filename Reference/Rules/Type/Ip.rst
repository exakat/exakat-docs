.. _type-ip:

.. _ip:

Ip
++

.. meta::
	:description:
		Ip: This rule lists hardocded IPs in the source.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ip
	:twitter:description: Ip: This rule lists hardocded IPs in the source
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ip
	:og:type: article
	:og:description: This rule lists hardocded IPs in the source
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Type/Ip.html
	:og:locale: en
This rule lists hardocded IPs in the source. Such IPs cannot be changed, and may produce unexpected results. 

.. code-block:: php
   
   <?php
   
   $ip = '123.34.56.227';
   $a = '3627734755';
   $a = '000000000330.0000000072.00000000326.0343';
   
   ?>

See also `IP converter <https://h.43z.one/ipconverter/>`_.

Connex PHP features
-------------------

  + `ip <https://php-dictionary.readthedocs.io/en/latest/dictionary/ip.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Ip                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


