.. _classes-thisisnotforstatic:

.. _$this-is-not-for-static-methods:

$this Is Not For Static Methods
+++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		$this Is Not For Static Methods: Static methods shouldn't use $this variable.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: $this Is Not For Static Methods
	:twitter:description: $this Is Not For Static Methods: Static methods shouldn't use $this variable
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: $this Is Not For Static Methods
	:og:type: article
	:og:description: Static methods shouldn't use $this variable
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/ThisIsNotForStatic.html
	:og:locale: en
  `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods shouldn't use `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable.

`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable represents an object, the current object. It is not compatible with a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, which may operate without any object. 

While executing a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ method, `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is actually set to `NULL <https://www.php.net/manual/en/language.types.null.php>`_.

.. code-block:: php
   
   <?php
   
   class foo {
       static $staticProperty = 1;
   
       // Static methods should use static properties
       static public function count() {
           return self::$staticProperty++;
       }
       
       // Static methods can't use $this
       static public function bar() {
           return $this->a;   // No $this usage in a static method
       }
   }
   
   ?>

See also `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Using+%24this+when+not+in+object+context+.html>`_



Connex PHP features
-------------------

  + `static <https://php-dictionary.readthedocs.io/en/latest/dictionary/static.ini.html>`_
  + `method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Remove the static keyword on the method, and update all calls to this method to use $this
* Remove the usage of $this in the method, replacing it with static properties
* Make $this an argument (and change its name) : then, make the method a function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ThisIsNotForStatic                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-static-this <https://github.com/dseguy/clearPHP/tree/master/rules/no-static-this.md>`__                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


