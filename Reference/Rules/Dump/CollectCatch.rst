.. _dump-collectcatch:

.. _collect-catch-calls:

Collect Catch Calls
+++++++++++++++++++

.. meta::
	:description:
		Collect Catch Calls: This analysis collects all catch command usage, along with the exception caught and the calling method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Collect Catch Calls
	:twitter:description: Collect Catch Calls: This analysis collects all catch command usage, along with the exception caught and the calling method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Collect Catch Calls
	:og:type: article
	:og:description: This analysis collects all catch command usage, along with the exception caught and the calling method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Catch Calls.html
	:og:locale: en
This analysis collects all catch command usage, along with the `exception <https://www.php.net/exception>`_ caught and the calling method.

.. code-block:: php
   
   <?php
   
   function foo() {
   	try {
   		// more code
   	} catch (Exception $e) {
   	
   	}
   }
   
   ?>

See also `Catch <https://www.php.net/manual/en/language.exceptions.php#language.exceptions.catch>`_.

Connex PHP features
-------------------

  + `catch <https://php-dictionary.readthedocs.io/en/latest/dictionary/catch.ini.html>`_
  + `try <https://php-dictionary.readthedocs.io/en/latest/dictionary/try.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectCatch                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
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


