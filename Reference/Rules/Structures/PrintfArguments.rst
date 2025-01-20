.. _structures-printfarguments:

.. _printf-number-of-arguments:

Printf Number Of Arguments
++++++++++++++++++++++++++

.. meta::
	:description:
		Printf Number Of Arguments: The number of arguments provided to printf(), vprintf() and vsprintf() doesn't match the format string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Printf Number Of Arguments
	:twitter:description: Printf Number Of Arguments: The number of arguments provided to printf(), vprintf() and vsprintf() doesn't match the format string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Printf Number Of Arguments
	:og:type: article
	:og:description: The number of arguments provided to printf(), vprintf() and vsprintf() doesn't match the format string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Printf Number Of Arguments.html
	:og:locale: en
The number of arguments provided to `printf() <https://www.php.net/printf>`_, `vprintf() <https://www.php.net/vprintf>`_ and `vsprintf() <https://www.php.net/vsprintf>`_ doesn't match the format string.

Extra arguments are ignored, and are dead code as such. Missing arguments are reported with a warning, and nothing is displayed.

Omitted arguments produce an `error <https://www.php.net/error>`_.

.. code-block:: php
   
   <?php
   
   // not enough arguments 
   printf(' a %s ', $a1); 
   // OK
   printf(' a %s ', $a1, $a2); 
   // too many arguments 
   printf(' a %s ', $a1, $a2, $a3); 
   
   // not enough arguments
   sprintf(' a %s ', $a1); 
   // OK
   \sprintf(' a %s ', $a1, $a2); 
   // too many arguments
   sprintf(' a %s ', $a1, $a2, $a3); 
   
   ?>

See also `printf <https://www.php.net/printf>`_, `sprintf <https://www.php.net/sprintf>`_ and `vsprintf <https://www.php.net/vsprintf>`_.

Connex PHP features
-------------------

  + `print <https://php-dictionary.readthedocs.io/en/latest/dictionary/print.ini.html>`_


Suggestions
___________

* Sync the number of argument with the format command




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PrintfArguments                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.1                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-phpipam-structures-printfarguments`                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


