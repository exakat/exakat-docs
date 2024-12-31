.. _php-assertionusage:

.. _assertions:

Assertions
++++++++++

.. meta\:\:
	:description:
		Assertions: Usage of assertions, to add checks within PHP code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Assertions
	:twitter:description: Assertions: Usage of assertions, to add checks within PHP code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Assertions
	:og:type: article
	:og:description: Usage of assertions, to add checks within PHP code
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/AssertionUsage.html
	:og:locale: en
  Usage of assertions, to add checks within PHP code.

Assertions should be used as a debugging feature only. You may use them for sanity-checks that test for conditions that should always be `TRUE <https://www.php.net/TRUE>`_ and that indicate some programming errors if not or to check for the presence of certain features like extension functions or certain system limits and features.

.. code-block:: php
   
   <?php
   
   function foo($string) {
       assert(!empty($string), 'An empty string was provided!');
       
       echo '['.$string.']';
   }
   
   ?>

See also `assert <https://www.php.net/assert>`_.

Connex PHP features
-------------------

  + `assertion <https://php-dictionary.readthedocs.io/en/latest/dictionary/assertion.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/AssertionUsage                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


