.. _functions-funcgetargmodified:

.. _func\_get\_arg()-modified:

func_get_arg() Modified
+++++++++++++++++++++++

.. meta::
	:description:
		func_get_arg() Modified: func_get_arg() and func_get_args() used to report the calling value of the argument until PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: func_get_arg() Modified
	:twitter:description: func_get_arg() Modified: func_get_arg() and func_get_args() used to report the calling value of the argument until PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: func_get_arg() Modified
	:og:type: article
	:og:description: func_get_arg() and func_get_args() used to report the calling value of the argument until PHP 7
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/func_get_arg() Modified.html
	:og:locale: en
`func_get_arg() <https://www.php.net/func_get_arg>`_ and `func_get_args() <https://www.php.net/func_get_args>`_ used to report the calling value of the argument until PHP 7. 

Since PHP 7, it is reporting the value of the argument at calling time, which may have been modified by a previous instruction. 

This code will display 1 in PHP 7, and 0 in PHP 5.

.. code-block:: php
   
   <?php
   
   function x($a) {
       print func_get_arg(0);  // 0 
       $a++;
       print func_get_arg(0);  // 1
   }
   
   x(0);
   ?>
Connex PHP features
-------------------

  + `arbitrary-argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/arbitrary-argument.ini.html>`_


Suggestions
___________

* Use func_get_arg() early in the function.
* Avoir mixing func_get_args() and direct access to the parameters.
* Avoir using func_get_args() and specifying parameters.
* Avoir modifying parameters.




Specs
_____

+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Functions/funcGetArgModified                                                                                                                                           |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                  |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                    |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Major                                                                                                                                                                  |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                        |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.0                                                                                                                                                                |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                                                   |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


