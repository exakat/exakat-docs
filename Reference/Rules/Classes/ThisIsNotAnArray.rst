.. _classes-thisisnotanarray:

.. _$this-is-not-an-array:

$this Is Not An Array
+++++++++++++++++++++

.. meta::
	:description:
		$this Is Not An Array: ``$this`` variable represents the current object and it is not an array.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: $this Is Not An Array
	:twitter:description: $this Is Not An Array: ``$this`` variable represents the current object and it is not an array
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: $this Is Not An Array
	:og:type: article
	:og:description: ``$this`` variable represents the current object and it is not an array
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/$this Is Not An Array.html
	:og:locale: en
``$this`` variable represents the current object and it is not an array. 

This is unless the class (or its parents) has the ``ArrayAccess`` interface, or extends ``ArrayObject`` or ``SimpleXMLElement``.

.. code-block:: php
   
   <?php
   
   // $this is an array
   class Foo extends ArrayAccess {
       function bar() {
           ++$this[3];
       }
   }
   
   // $this is not an array
   class Foo2 {
       function bar() {
           ++$this[3];
       }
   }
   
   ?>

See also `ArrayAccess <https://www.php.net/manual/en/class.arrayaccess.php>`_, `ArrayObject <https://www.php.net/manual/en/class.arrayobject.php>`_ and `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Related PHP errors 
-------------------

  + `Cannot use object of type %s as array <https://php-errors.readthedocs.io/en/latest/messages/cannot-use-object-of-type-%25s-as-array.html>`_



Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_


Suggestions
___________

* Extends ``ArrayObject``, or a class that extends it, to use ``$this`` as an array too.
* Implements ``ArrayAccess`` to use ``$this`` as an array too.
* Use a property in the current class to store the data, instead of $this directly.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ThisIsNotAnArray                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


