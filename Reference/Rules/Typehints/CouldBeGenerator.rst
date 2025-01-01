.. _typehints-couldbegenerator:

.. _could-be-generator:

Could Be Generator
++++++++++++++++++

.. meta::
	:description:
		Could Be Generator: This rule reports methods, functions.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Generator
	:twitter:description: Could Be Generator: This rule reports methods, functions
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Generator
	:og:type: article
	:og:description: This rule reports methods, functions
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeGenerator.html
	:og:locale: en
This rule reports methods, functions... where the return value may be typed ``Generator``. This is the case when the body of the function uses the ``yield`` and ``yield from`` keyword.

.. code-block:: php
   
   <?php
   
   // Yield makes foo() a generator
   function foo() {
       yield 1; 
       // Returns an int
       return $b + 8;
   }
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `yield <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield.ini.html>`_
  + `yield-from <https://php-dictionary.readthedocs.io/en/latest/dictionary/yield-from.ini.html>`_


Suggestions
___________

* Add `\Generator` typehint to the method.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeGenerator                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.2                                                                                                                   |
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


