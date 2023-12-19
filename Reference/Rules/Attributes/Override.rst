.. _attributes-override:

.. _override:

Override
++++++++

  Override is a native PHP `attribute <https://www.php.net/attribute>`_. It was introduced in PHP 8.3, and was not available before. 

In fact, `static <https://www.php.net/manual/en/language.oop5.static.php>`_ analysis can perform that check on previous versions of PHP.

Override signals that the class has a method which overrides the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_'s definition. If there is no such method in a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, an `error <https://www.php.net/error>`_ is raised.

This analysis is not valid after PHP 8.3, as PHP does that itself.


.. code-block:: php
   
   <?php
   
   class x {
   	function foo() {}
   }
   
   class y extends x {
   	// OK, there is a method in the class above
   	#[Override]
   	function foo() {}
   
   	// KO, there is no such method in the class above
   	#[Override]
   	function hoo() {}
   }
   
   
   ?>

See also `PHP RFC: Marking overridden methods (#[\Override]) <https://wiki.php.net/rfc/marking_overriden_methods>`_ and `PHP 8.3 RFC: Marking overridden methods (#[\Override]) <https://php.watch/rfcs/marking_overriden_methods>`_.


Suggestions
___________

* Change the name of the current method to match an existing one
* Remove the method
* Remove the attribute




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/Override                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.3 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


