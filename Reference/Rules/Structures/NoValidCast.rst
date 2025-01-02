.. _structures-novalidcast:

.. _no-valid-cast:

No Valid Cast
+++++++++++++

.. meta::
	:description:
		No Valid Cast: This cast generates an error, as there is no way to convert an object to an int.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Valid Cast
	:twitter:description: No Valid Cast: This cast generates an error, as there is no way to convert an object to an int
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Valid Cast
	:og:type: article
	:og:description: This cast generates an error, as there is no way to convert an object to an int
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Valid Cast.html
	:og:locale: en
This cast generates an `error <https://www.php.net/error>`_, as there is no way to convert an object to an int. 

The `result <https://www.php.net/result>`_ will be 1. 

This rule applies to float and int. This doesn't apply to string cast, as the magic method `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ allows for such conversions.

.. code-block:: php
   
   <?php
   
   $a = (int) foo();
   
   function foo() : A {} 
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Object+of+class+stdClass+could+not+be+converted+to.html>`_



Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Suggestions
___________

* Create a method that convert the original object to the target type




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoValidCast                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


