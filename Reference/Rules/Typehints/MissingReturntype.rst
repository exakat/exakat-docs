.. _typehints-missingreturntype:

.. _missing-some-returntype:

Missing Some Returntype
+++++++++++++++++++++++

.. meta::
	:description:
		Missing Some Returntype: The specified typehints are not compatible with the returned values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Missing Some Returntype
	:twitter:description: Missing Some Returntype: The specified typehints are not compatible with the returned values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Missing Some Returntype
	:og:type: article
	:og:description: The specified typehints are not compatible with the returned values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Missing Some Returntype.html
	:og:locale: en
The specified typehints are not compatible with the returned values. 

The code of the method may return other types, which are not specified and will lead to a PHP fatal `error <https://www.php.net/error>`_. It is the case for insufficient typehints, when a typehint is missing, or inconsistent typehints, when the method returns varied types. 
The analysis reports a method when it finds other return types than the one expected. In the case of multiple typehints, as for the last example, the PHP code may require an upgrade to PHP 8.0.

.. code-block:: php
   
   <?php
   
   // correct return typehint
   function fooSN() : ?string  {
       return shell_exec('ls -hla');
   }
   
   // insufficient return typehint
   // shell_exec() may return null or string. Here, only string in specified for fooS, and that may lead to a Fatal error
   function fooS() : string  {
       return shell_exec('ls -hla');
   }
   
   // inconsistent return typehint
   function bar() : int {
       return rand(0, 10) ? 1 : "b";
   }
   
   ?>
Related PHP errors 
-------------------

  + `Return value of %s() must be of the type %s, %s returned <https://php-errors.readthedocs.io/en/latest/messages/%25s%25s%25s%28%29%3A+Return+value+must+be+of+type+%25s%2C+%25s+returned.html>`_



Connex PHP features
-------------------

  + `return-typehint <https://php-dictionary.readthedocs.io/en/latest/dictionary/return-typehint.ini.html>`_


Suggestions
___________

* Update the typehint to accept more types
* Update the code of the method to fit the expected returntype




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/MissingReturntype                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.7                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


