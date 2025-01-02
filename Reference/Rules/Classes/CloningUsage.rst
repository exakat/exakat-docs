.. _classes-cloningusage:

.. _clone-usage:

Clone Usage
+++++++++++

.. meta::
	:description:
		Clone Usage: This rule lists of all clone expressions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Clone Usage
	:twitter:description: Clone Usage: This rule lists of all clone expressions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Clone Usage
	:og:type: article
	:og:description: This rule lists of all clone expressions
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Clone Usage.html
	:og:locale: en
This rule lists of all clone expressions. Cloning objects leads to creating a new object without calling the constructor, but rather the ``__clone`` method, when available.

.. code-block:: php
   
   <?php
       $dateTime = new DateTime();
       echo (clone $dateTime)->format('Y');
   ?>

See also `Object cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_.

Connex PHP features
-------------------

  + `clone <https://php-dictionary.readthedocs.io/en/latest/dictionary/clone.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CloningUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


