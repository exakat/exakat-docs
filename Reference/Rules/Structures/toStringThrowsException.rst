.. _structures-tostringthrowsexception:

.. _\_\_tostring()-throws-exception:

__toString() Throws Exception
+++++++++++++++++++++++++++++

  Magical method `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ can't throw exceptions.

In fact, `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ may not let an `exception <https://www.php.net/exception>`_ pass. If it throw an `exception <https://www.php.net/exception>`_, but must catch it. If an underlying method throws an `exception <https://www.php.net/exception>`_, it must be caught.



A fatal `error <https://www.php.net/error>`_ is displayed, when an `exception <https://www.php.net/exception>`_ is not intercepted in the `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ function.

.. code-block:: php
   
   <?php
   
   class myString {
       private $string = null;
       
       public function __construct($string) {
           $this->string = $string;
       }
       
       public function __toString() {
           // Do not throw exceptions in __toString
           if (!is_string($this->string)) {
               throw new Exception("$this->string is not a string!!");
           }
           
           return $this->string;
       }
   }   
   
   ?>

See also __toString().

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Method+myString%3A%3A__toString%28%29+must+not+throw+an+exception.html>`_



Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_
  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Remove any usage of exception from __toString() magic method




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/toStringThrowsException                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


