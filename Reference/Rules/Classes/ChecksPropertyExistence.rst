.. _classes-checkspropertyexistence:

.. _checks-property-existence:

Checks Property Existence
+++++++++++++++++++++++++

.. meta::
	:description:
		Checks Property Existence: This analysis reports checks property existence.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Checks Property Existence
	:twitter:description: Checks Property Existence: This analysis reports checks property existence
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Checks Property Existence
	:og:type: article
	:og:description: This analysis reports checks property existence
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/ChecksPropertyExistence.html
	:og:locale: en
This analysis reports checks property existence. 

In PHP 8.2, non-specified properties are discouraged : they should always be defined in the class code. When this guideline is applied, properties always exists, and a call to `property_exists() <https://www.php.net/property_exists>`_ is now useless.

Some situations are still legit : 
+ When the class is ``stdClass``, where no property is initially defined. This may be the case of JSON data, or arrays cast to objects.
+ When the class uses magic methods, in particular `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_.
In this analysis, `isset() <https://www.www.php.net/isset>`_ and `property_exists() <https://www.php.net/property_exists>`_ are both used to detect this checking behavior. `property_exists() <https://www.php.net/property_exists>`_ is actually the only method to actually check the existence, since `isset() <https://www.www.php.net/isset>`_ will confuse non-existing properties and ``null``. 

While the behavior is deprecated in PHP 8.2, it is recommended to review older code and remove it. It will both ensure forward compatibility and cleaner, faster local code.

.. code-block:: php
   
   <?php
   
   class x {
       private $a = 1;
       
       function foo() {
           $this->cache = $this->a + 1;
       }
   
   }
   
   ?>
Connex PHP features
-------------------

  + `stdclass <https://php-dictionary.readthedocs.io/en/latest/dictionary/stdclass.ini.html>`_
  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ChecksPropertyExistence                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.3                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`undefined-properties`                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


