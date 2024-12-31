.. _variables-constanttypo:

.. _constant-typo-looks-like-a-variable:

Constant Typo Looks Like A Variable
+++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Constant Typo Looks Like A Variable: A constant bears the same name as a variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Typo Looks Like A Variable
	:twitter:description: Constant Typo Looks Like A Variable: A constant bears the same name as a variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Typo Looks Like A Variable
	:og:type: article
	:og:description: A constant bears the same name as a variable
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Variables/ConstantTypo.html
	:og:locale: en
  A constant bears the same name as a variable. This might be a typo.

When the constant doesn't exist, PHP 8.0 yields a Fatal `Error <https://www.php.net/error>`_ and stops execution. PHP 7.4 turns the undefined constant into its string equivalent. 
This analysis is case sensitive.

.. code-block:: php
   
   <?php
   
   // Get an object or null
   $object = foo(); 
   
   // PHP 8.0 stops here, with a Fatal Error
   // PHP 7.4 makes this a string, and the condition is always true
   if (!empty(object)) {
       // In PHP 7.4, this is not protected by the condition, and may yield an error.
       $object->doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_
  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Suggestions
___________

* Add a $ sign to the constant
* Use a different name for the variable, or the constant




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/ConstantTypo                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`undefined-constants`                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


