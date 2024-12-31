.. _functions-couldbestaticclosure:

.. _could-be-static-closure:

Could Be Static Closure
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Could Be Static Closure: Closure and arrow functions may be static, and prevent the import of ``$this``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Static Closure
	:twitter:description: Could Be Static Closure: Closure and arrow functions may be static, and prevent the import of ``$this``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Static Closure
	:og:type: article
	:og:description: Closure and arrow functions may be static, and prevent the import of ``$this``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/CouldBeStaticClosure.html
	:og:locale: en
  `Closure <https://www.php.net/manual/en/class.`closure <https://www.php.net/closure>`_.php>`_ and arrow functions may be `static <https://www.php.net/manual/en/language.oop5.static.php>`_, and prevent the import of ``$this``. 

By preventing the useless import of ``$this``, you avoid useless work. 

This also has the added value to prevent the usage of ``$this`` from the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_. This is a good security practice.
This is a micro-optimisation. Apply it in case of intensive usage.

.. code-block:: php
   
   <?php
   
   class Foo
   {
       function __construct()
       {
   
           // Not possible to use $this
           $func = static function() {
               var_dump($this);
           };
           $func();
   
           // Normal import of $this
           $closure = function() {
               var_dump($this);
           };
       }
   };
   new Foo();
   
   ?>

See also `Anonymous functions <https://www.php.net/manual/en/functions.anonymous.php>`_, `GeneratedHydrator <https://github.com/Ocramius/GeneratedHydrator/releases/tag/3.0.0>`_ and `Static anonymous functions <https://www.php.net/manual/en/functions.anonymous.php#functions.anonymous-functions.static>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Add the static keyword to the closure.
* Make actual usage of $this in the closure.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/CouldBeStaticClosure                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-functions-couldbestaticclosure`                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


