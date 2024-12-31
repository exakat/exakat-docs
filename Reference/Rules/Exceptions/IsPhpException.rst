.. _exceptions-isphpexception:

.. _php-exception:

PHP Exception
+++++++++++++

.. meta\:\:
	:description:
		PHP Exception: Mark an exception as a native exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Exception
	:twitter:description: PHP Exception: Mark an exception as a native exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Exception
	:og:type: article
	:og:description: Mark an exception as a native exception
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Exceptions/IsPhpException.html
	:og:locale: en
  Mark an `exception <https://www.php.net/exception>`_ as a native `exception <https://www.php.net/exception>`_. They may come from PHP standard distribution or an extension.

.. code-block:: php
   
   <?php
   
   // From the native set
   $a = new LogicException('Logic error');
   throw $a;
   
   // From an extension
   throw new ZookeeperException('Zookeeper error');
   
   ?>

See also `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/IsPhpException                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


