.. _classes-shoulddeepclone:

.. _should-deep-clone:

Should Deep Clone
+++++++++++++++++

  By default, PHP makes a shallow clone. It only clone the scalars, and keep the reference to any object already referenced. This means that the cloned object and its original share any object they hold as property.

This is where the magic method `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ comes into play. It is called, when defined, at clone time, so that the cloned object may clone all the needed sub-objects.

It is recommended to use the `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_ method whenever the objects hold objects.

.. code-block:: php
   
   <?php
   
   class a {
       public $b = null;
       
       function __construct() {
           $this->b =  new Stdclass();
           $this->b->c = 1;
       }
   }
   
   class ab extends a {
       function __clone() {
           $this->b = clone $this->b;
       }
   }
   
   // class A is shallow clone, so $a->b is not cloned
   $a = new a();
   $b = clone $a;
   $a->b->c = 3;
   echo $b->b->c;
   // displays 3
   
   // class Ab is deep clone, so $a->b is cloned
   $a = new ab();
   $b = clone $a;
   $a->b->c = 3;
   echo $b->b->c;
   // displays 1
   
   ?>

See also `PHP Clone and Shallow vs Deep Copying <http://jacob-walker.com/blog/php-clone-and-shallow-vs-deep-copying.html>`_ and `Cloning objects <https://www.php.net/manual/en/language.oop5.cloning.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ShouldDeepClone                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | clone                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


