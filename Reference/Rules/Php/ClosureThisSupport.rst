.. _php-closurethissupport:

.. _closure-may-use-$this:

Closure May Use $this
+++++++++++++++++++++

.. meta::
	:description:
		Closure May Use $this: $this is automatically accessible to closures.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Closure May Use $this
	:twitter:description: Closure May Use $this: $this is automatically accessible to closures
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Closure May Use $this
	:og:type: article
	:og:description: $this is automatically accessible to closures
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ClosureThisSupport.html
	:og:locale: en
`$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is automatically accessible to closures.

When closures were introduced in PHP, they couldn't use the `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable, making is cumbersome to access local properties when the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ was created within an object. 
This is not the case anymore since PHP 5.4.

.. code-block:: php
   
   <?php
   
   // Invalid code in PHP 5.4 and less
   class Test
   {
       public function testing()
       {
           return function() {
               var_dump($this);
           };
       }
   }
   
   $object = new Test;
   $function = $object->testing();
   $function();
       
   ?>

See also `Anonymous functions <https://www.php.net/manual/en/functions.anonymous.php>`_.

Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_


Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Php/ClosureThisSupport                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 5.4 and older                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 5.4                                                                                                                              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


