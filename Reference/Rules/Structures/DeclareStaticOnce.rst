.. _structures-declarestaticonce:

.. _declare-static-once:

Declare Static Once
+++++++++++++++++++

.. meta::
	:description:
		Declare Static Once: Global and static variables should be declared only once in a method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Declare Static Once
	:twitter:description: Declare Static Once: Global and static variables should be declared only once in a method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Declare Static Once
	:og:type: article
	:og:description: Global and static variables should be declared only once in a method
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/DeclareStaticOnce.html
	:og:locale: en
Global and `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables should be declared only once in a method. It is also recommended to configure it at the beginning of the method. This could be refined by defining the variable at the last common moment, though it lacks readability.
Defining `static <https://www.php.net/manual/en/language.oop5.static.php>`_ or global methods late is a micro-optimisation.

.. code-block:: php
   
   <?php
   
   function foo() {
       if (rand(0, 1)) {
           static $x;
           
           ++$x;
       } else {
           static $x;
           
           --$x;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_


Suggestions
___________

* Remove duplicate static and global calls
* Move the static and global calls to the beginning of the method
* Refactor the static and global variable to properties




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DeclareStaticOnce                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.3 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


