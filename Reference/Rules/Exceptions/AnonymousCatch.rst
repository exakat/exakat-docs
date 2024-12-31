.. _exceptions-anonymouscatch:

.. _anonymous-catch:

Anonymous Catch
+++++++++++++++

.. meta\:\:
	:description:
		Anonymous Catch: It is possible to omit the variable when using a catch clause.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Anonymous Catch
	:twitter:description: Anonymous Catch: It is possible to omit the variable when using a catch clause
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Anonymous Catch
	:og:type: article
	:og:description: It is possible to omit the variable when using a catch clause
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/AnonymousCatch.html
	:og:locale: en
  It is possible to omit the variable when using a catch clause. It will catch the `exception <https://www.php.net/exception>`_, but it will not provide the details of the caught `exception <https://www.php.net/exception>`_.

.. code-block:: php
   
   <?php
   
   try {
   
   } catch (Exception) {
   
   }
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/AnonymousCatch                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP80 <ruleset-CompatibilityPHP80>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


