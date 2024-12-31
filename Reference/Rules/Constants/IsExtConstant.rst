.. _constants-isextconstant:

.. _is-an-extension-constant:

Is An Extension Constant
++++++++++++++++++++++++

.. meta\:\:
	:description:
		Is An Extension Constant: Mark a constant if it belongs to a known extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is An Extension Constant
	:twitter:description: Is An Extension Constant: Mark a constant if it belongs to a known extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is An Extension Constant
	:og:type: article
	:og:description: Mark a constant if it belongs to a known extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Constants/IsExtConstant.html
	:og:locale: en
  Mark a constant if it belongs to a known extension.

.. code-block:: php
   
   <?php
   
   // JSON_HEX_AMP is a constant from ext/json
   echo json_encode($object, JSON_HEX_AMP);
   
   // JSON_HEX_AMP is a constant from ext/json
   echo json_encode($object, JSON_HOAX_AMP);
   
   ?>

See also `Supported PHP Extensions <http://exakat.readthedocs.io/en/latest/Annex.html#supported-php-extensions>`_.

Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/IsExtConstant                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


