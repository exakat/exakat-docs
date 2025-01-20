.. _structures-invalidcast:

.. _invalid-cast:

Invalid Cast
++++++++++++

.. meta::
	:description:
		Invalid Cast: Some cast operations not permitted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Invalid Cast
	:twitter:description: Invalid Cast: Some cast operations not permitted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Invalid Cast
	:og:type: article
	:og:description: Some cast operations not permitted
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Invalid Cast.html
	:og:locale: en
Some cast operations not permitted. 

+ (string) on an object whose class doesn't have a ``__toString`` method
+ (int) on any object, except certain PHP native ones
+ (string) on an array: this will produce the ``Array`` string, which is useless.



.. code-block:: php
   
   <?php
   
   class Foo {}
   
   (string) new Foo();     // Error
   
   print (string) array(); // Array 
   
   ?>
Related PHP errors 
-------------------

  + `Object of class stdClass could not be converted to float <https://php-errors.readthedocs.io/en/latest/messages/object-of-class-%25s-could-not-be-converted-to-float.html>`_
  + `Object of class stdClass could not be converted to int <https://php-errors.readthedocs.io/en/latest/messages/object-of-class-%25s-could-not-be-converted-to-int.html>`_
  + `Array to string conversion <https://php-errors.readthedocs.io/en/latest/messages/array-to-string-conversion.html>`_



Connex PHP features
-------------------

  + `cast <https://php-dictionary.readthedocs.io/en/latest/dictionary/cast.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidCast                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------+


