.. _php-cantusereturnvalueinwritecontext:

.. _cant-use-return-value-in-write-context:

Cant Use Return Value In Write Context
++++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Cant Use Return Value In Write Context: empty() used to work only on data containers, such as variables.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cant Use Return Value In Write Context
	:twitter:description: Cant Use Return Value In Write Context: empty() used to work only on data containers, such as variables
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cant Use Return Value In Write Context
	:og:type: article
	:og:description: empty() used to work only on data containers, such as variables
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/CantUseReturnValueInWriteContext.html
	:og:locale: en
  empty() used to work only on data containers, such as variables. Until PHP 5.5, it was not possible to use directly expressions, such as functioncalls, inside an empty() function call : they were met with a 'Can't use function return value in write context' fatal `error <https://www.php.net/error>`_. 
This also applies to methodcalls, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or not.

.. code-block:: php
   
   <?php
   
   function foo($boolean) {
       return $boolean;
   }
   
   // Valid since PHP 5.5
   echo empty(foo(true)) : 'true' : 'false';
   
   ?>

See also `Cant Use Return Value In Write Context <https://stackoverflow.com/questions/1075534/cant-use-method-return-value-in-write-context>`_.

Connex PHP features
-------------------

  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/CantUseReturnValueInWriteContext                                                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.5 and more recent                                                                                                                                                                 |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


