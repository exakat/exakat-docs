.. _structures-duplicatecalls:

.. _duplicate-calls:

Duplicate Calls
+++++++++++++++

.. meta::
	:description:
		Duplicate Calls: Duplicate calls within the same context.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Duplicate Calls
	:twitter:description: Duplicate Calls: Duplicate calls within the same context
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Duplicate Calls
	:og:type: article
	:og:description: Duplicate calls within the same context
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Duplicate Calls.html
	:og:locale: en
Duplicate calls within the same context. They should be called once, and then cached in a variable for reuse. 

This saves a lot of time of execution and reexecution of the same code. It is a micro-optimisation in case of a simple property fetch, but it may be more costly.

.. code-block:: php
   
   <?php
   
   function foo($name) {
       // The name decoration on the string is done twice. Once should be cached in a variable.
       echo "Hello, ".ucfirst(strtolower($name))."<br />";
   
       $query = 'Insert into visitors values ("'.ucfirst(strtolower($name)).'")';
       $res = $db->query($query);
   }
   
   ?>

See also `Userland naming Guide <https://www.php.net/manual/en/userlandnaming.php>`_.

Connex PHP features
-------------------

  + `calls <https://php-dictionary.readthedocs.io/en/latest/dictionary/calls.ini.html>`_
  + `micro-optimisation <https://php-dictionary.readthedocs.io/en/latest/dictionary/micro-optimisation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DuplicateCalls                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-duplicated-code <https://github.com/dseguy/clearPHP/tree/master/rules/no-duplicated-code.md>`__                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


