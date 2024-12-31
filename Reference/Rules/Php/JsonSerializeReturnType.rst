.. _php-jsonserializereturntype:

.. _php-native-interfaces-and-return-type:

PHP Native Interfaces and Return Type
+++++++++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		PHP Native Interfaces and Return Type: Native PHP interface which define a type, expect the derived methods to use the same time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Native Interfaces and Return Type
	:twitter:description: PHP Native Interfaces and Return Type: Native PHP interface which define a type, expect the derived methods to use the same time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Native Interfaces and Return Type
	:og:type: article
	:og:description: Native PHP interface which define a type, expect the derived methods to use the same time
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/JsonSerializeReturnType.html
	:og:locale: en
  Native PHP interface which define a type, expect the derived methods to use the same time. In particular, a mixed return type was added to the jsonSerialize() of the JsonSerialize PHP interface. 

In PHP 8.1, the mixed return type is now enforced, and a deprecated notice is displayed.

One solution is to add the good return type, or to use the `#[`ReturnTypeWillChange <https://www.php.net/returntypewillchange>`_]` `attribute <https://www.php.net/attribute>`_.
This rule covers the following interfaces : 

+ `ArrayAccess <https://www.php.net/manual/en/class.`arrayaccess <https://www.php.net/arrayaccess>`_.php>`_
+ `Countable <https://www.php.net/countable>`_
+ `Exception <https://www.php.net/exception>`_
+ `FilterIterator <https://www.php.net/filteriterator>`_
+ `Iterator <https://www.php.net/iterator>`_
+ `JsonSerializable <https://www.php.net/jsonserializable>`_
+ `php_user_filter <https://www.php.net/php_user_filter>`_
+ `SessionHandlerInterface <https://www.php.net/sessionhandlerinterface>`_

.. code-block:: php
   
   <?php
       class MyJsonSerialize implements jsonserialize { 
           function jsonserialize() : int {}
       }
   ?>

See also `JsonSerializable::jsonSerialize <https://www.php.net/manual/en/jsonserializable.jsonserialize.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Return+type+of+x%3A%3Ajsonserialize%28%29+should+either+be+compatible+with+JsonSerializable%3A%3AjsonSerialize%28%29%3A+mixed%2C+or+the+%23%5B%5CReturnTypeWillChange%5D+attribute+should+be+used+to+temporarily+suppress+the+notice.html>`_



Connex PHP features
-------------------

  + `json <https://php-dictionary.readthedocs.io/en/latest/dictionary/json.ini.html>`_


Suggestions
___________

* Add the mixed returntype to all implementation of the jsonSerialize method
* Add the #[\ReturnTypeWillChange] attribute to the method




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/JsonSerializeReturnType                                                                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP81 <ruleset-CompatibilityPHP81>`, :ref:`Deprecated <ruleset-Deprecated>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.0                                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


