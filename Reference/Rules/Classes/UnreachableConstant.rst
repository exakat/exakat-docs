.. _classes-unreachableconstant:

.. _unreachable-class-constant:

Unreachable Class Constant
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Unreachable Class Constant: Class constants may be unreachable due to visibility configuration.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unreachable Class Constant
	:twitter:description: Unreachable Class Constant: Class constants may be unreachable due to visibility configuration
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unreachable Class Constant
	:og:type: article
	:og:description: Class constants may be unreachable due to visibility configuration
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/UnreachableConstant.html
	:og:locale: en
  Class constants may be unreachable due to visibility configuration. 

Since PHP 7.1, class constants support visibility. Their usage may be restricted to the current class, or ``private``, to classes that extends or are extended by the current class, or ``protected``. They may also be ``public``, just like it was before.

.. code-block:: php
   
   <?php
   
   class Foo{
       private const PRIVATE = 1;
               const PUBLIC = 3;
   }
   
   // PHP 7.1- and older
   echo Foo::PUBLIC;
   
   // This is not accessible
   echo Foo::PRIVATE;
   
   ?>

See also `Class Constant <https://www.php.net/manual/en/language.oop5.constants.php>`_ and `PHP RFC: Support Class Constant Visibility <https://wiki.php.net/rfc/class_const_visibility>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+access+private+const+.html>`_



Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Make the class constant protected, when the call to the constant is inside a related class.
* Create another constant, that may be accessible
* Make the class constant public




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UnreachableConstant                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


