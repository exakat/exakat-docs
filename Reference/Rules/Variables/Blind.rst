.. _variables-blind:

.. _blind-variables:

Blind Variables
+++++++++++++++

.. meta::
	:description:
		Blind Variables: Blind variables are that are used in foreach or for structure, for managing the loop itself.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Blind Variables
	:twitter:description: Blind Variables: Blind variables are that are used in foreach or for structure, for managing the loop itself
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Blind Variables
	:og:type: article
	:og:description: Blind variables are that are used in foreach or for structure, for managing the loop itself
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/Blind.html
	:og:locale: en
Blind variables are that are used in foreach or for structure, for managing the loop itself.

.. code-block:: php
   
   <?php
       foreach($array as $key => $value) {
           // $key and $value are blind values
       }
   
   ?>
Connex PHP features
-------------------

  + `blind-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/blind-variable.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Blind                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


