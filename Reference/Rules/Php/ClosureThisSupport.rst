.. _php-closurethissupport:

.. _closure-may-use-$this:

Closure May Use $this
+++++++++++++++++++++

  `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ is automatically accessible to closures.

When closures were introduced in PHP, they couldn't use the `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable, making is cumbersome to access local properties when the `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ was created within an object. 


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


This is not the case anymore since PHP 5.4.

See also `Anonymous functions <https://www.php.net/manual/en/functions.anonymous.php>`_.


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
| Changed Behavior | PHP 5.4 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                            |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Features         | closure, $this                                                                                                                       |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------+


