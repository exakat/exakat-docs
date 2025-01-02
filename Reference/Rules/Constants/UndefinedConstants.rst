.. _constants-undefinedconstants:

.. _undefined-constants:

Undefined Constants
+++++++++++++++++++

.. meta::
	:description:
		Undefined Constants: Constants definition can't be located.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Undefined Constants
	:twitter:description: Undefined Constants: Constants definition can't be located
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Undefined Constants
	:og:type: article
	:og:description: Constants definition can't be located
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Undefined Constants.html
	:og:locale: en
Constants definition can't be located.

Those constants are not defined in the code, and will raise errors, or use the fallback mechanism of being treated like a string. 
It is recommended to define them all, or to avoid using them.

.. code-block:: php
   
   <?php
   
   const A = 1;
   define('B', 2);
   
   // here, C is not defined in the code and is reported
   echo A.B.C;
   
   ?>

See also `Constants <https://www.php.net/manual/en/language.constants.php>`_.

Related PHP errors 
-------------------

  + `Undefined constant '%s' <https://php-errors.readthedocs.io/en/latest/messages/undefined-constant-%22%25s.html>`_



Connex PHP features
-------------------

  + `typo <https://php-dictionary.readthedocs.io/en/latest/dictionary/typo.ini.html>`_


Suggestions
___________

* Define the constant
* Fix the name of the constant
* Fix the namespace of the constant (Fully Qualified Name or use)
* Remove the usage of the constant




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/UndefinedConstants                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP72 <ruleset-CompatibilityPHP72>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`constant-typo-looks-like-a-variable`                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


