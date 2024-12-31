.. _php-nativeclasstypecompatibility:

.. _php-native-class-type-compatibility:

PHP Native Class Type Compatibility
+++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		PHP Native Class Type Compatibility: PHP enforces the method compatibility with native classes and interfaces.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Native Class Type Compatibility
	:twitter:description: PHP Native Class Type Compatibility: PHP enforces the method compatibility with native classes and interfaces
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Native Class Type Compatibility
	:og:type: article
	:og:description: PHP enforces the method compatibility with native classes and interfaces
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/NativeClassTypeCompatibility.html
	:og:locale: en
  PHP enforces the method compatibility with native classes and interfaces. 

This means that classes that extends native PHP classes or interfaces must declare compatible types. They can't omit typing, like it was the case until PHP 8.0.
This is needed for compatibility with PHP 8.0. This is probably good for older versions too, although it is not reported.

The `attribute <https://www.php.net/attribute>`_ ``ReturnTypeWillChange`` is taken into account by this rule. Note that it is not detected when auditing with PHP < 8.0, so it won't have effect until this version. The `attribute <https://www.php.net/attribute>`_ was declared in PHP 8.1, though it is also taken into account when auditing with PHP 8.0.

.. code-block:: php
   
   <?php
   
   class a extends RecursiveFilterIterator { 
   
       // fully declared method
       function hasChildren(): bool {
           return true;
       }
   
       // key() returns mixed. Omitting the type used to be quiet
       function key() {}
       
       //    #[\ReturnTypeWillChange] is taken into account 
   
   }
   ?>

See also method-compatibility.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Return+type+of+a%3A%3Akey%28%29+should+either+be+compatible+with+IteratorIterator%3A%3Akey%28%29%3A+mixed%2C+or+the+%23%5B%5CReturnTypeWillChange%5D+attribute+should+be+used+to+temporarily+suppress+the+notice.html>`_



Connex PHP features
-------------------

  + `returntypewillchange <https://php-dictionary.readthedocs.io/en/latest/dictionary/returntypewillchange.ini.html>`_
  + `type-covariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-covariance.ini.html>`_
  + `type-contravariance <https://php-dictionary.readthedocs.io/en/latest/dictionary/type-contravariance.ini.html>`_


Suggestions
___________

* Make sure the methods are compatible or identical to the parent's method signature.




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/NativeClassTypeCompatibility                                                                                                                                       |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.4                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


