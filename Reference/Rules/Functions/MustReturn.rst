.. _functions-mustreturn:

.. _must-return-methods:

Must Return Methods
+++++++++++++++++++

.. meta\:\:
	:description:
		Must Return Methods: The following methods are expected to return a value that will be used later.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Must Return Methods
	:twitter:description: Must Return Methods: The following methods are expected to return a value that will be used later
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Must Return Methods
	:og:type: article
	:og:description: The following methods are expected to return a value that will be used later
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/MustReturn.html
	:og:locale: en
  The following methods are expected to return a value that will be used later. Without return, they are useless.

Methods that must return are : `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__isset() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__sleep() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__set_state() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__invoke() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__debugInfo() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Methods that may not return, but are often expected to : `__call() <https://www.php.net/manual/en/language.oop5.magic.php>`_, `__callStatic() <https://www.php.net/manual/en/language.oop5.magic.php>`_.

.. code-block:: php
   
   <?php
   
   class foo {
       public function __isset($a) {
           // returning something useful
           return isset($this->$var[$a]);
       }
   
       public function __get($a) {
           $this->$a++;
           // not returning... 
       }
   
       public function __call($name, $args) {
           $this->$name(...$args);
           // not returning anything, but that's OK
       }
   
   }
   ?>
Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Add a return expression, with a valid data type
* Remove the return typehint




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/MustReturn                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


