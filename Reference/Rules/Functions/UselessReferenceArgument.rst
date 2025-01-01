.. _functions-uselessreferenceargument:

.. _useless-referenced-argument:

Useless Referenced Argument
+++++++++++++++++++++++++++

.. meta::
	:description:
		Useless Referenced Argument: The argument has a reference, and is only used for reading.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Referenced Argument
	:twitter:description: Useless Referenced Argument: The argument has a reference, and is only used for reading
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Referenced Argument
	:og:type: article
	:og:description: The argument has a reference, and is only used for reading
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UselessReferenceArgument.html
	:og:locale: en
The argument has a reference, and is only used for reading. 

This is probably a development artefact that was forgotten. It is better to remove it. 

This analysis also applies to `foreach() <https://www.php.net/manual/en/control-structures.foreach.php>`_ loops, that declare the blind variable as reference, then use the variable as an object, accessing properties and methods. When a variable contains an object, there is no need to declare a reference : it is a reference automatically.

.. code-block:: php
   
   <?php
   
   function foo($a, &$b, &$c) {
       // $c is passed by reference, but only read. The reference is useless.
       $b = $c + $a;
       // The reference is useful for $b
   }
   
   foreach ($array as &$element) {
       $element->method();
   }
   
   ?>

See also `Objects and references <https://www.php.net/manual/en/language.oop5.references.php>`_.

Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_
  + `argument <https://php-dictionary.readthedocs.io/en/latest/dictionary/argument.ini.html>`_


Suggestions
___________

* Remove the useless & from the argument
* Make an actual use of the argument before the end of the method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UselessReferenceArgument                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-functions-uselessreferenceargument`, :ref:`case-magento-functions-uselessreferenceargument`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


