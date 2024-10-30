.. _classes-noparent:

.. _class-without-parent:

Class Without Parent
++++++++++++++++++++

  Classes should not refer to ``parent`` when it is not extending another class. 

In PHP 7.4, it is a Deprecated warning. In PHP 7.3, it was a Fatal `error <https://www.php.net/error>`_, when the code was eventually executed. In PHP 8.0, PHP detects this `error <https://www.php.net/error>`_ at compile time, except for `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ keyword in a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_.

``parent`` usage in trait is detected. It is only reported when the trait is used inside a class without `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_, as the trait may also be used in another class, which has a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

.. code-block:: php
   
   <?php
   
   class x {
       function foo() {
           parent::foo();
       }
   }
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+use+%22%22parent%22%22+when+current+class+scope+has+no+parent.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+access+parent%3A%3A+when+current+class+scope+has+no+parent.html>`_



Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Update the class and make it extends another class
* Change the parent mention with a fully qualified name
* Remove the call to the parent altogether




Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/NoParent                                                                                                                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 1.9.0                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                                                                                                                      |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                                                                                          |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                                                                                               |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | Very high                                                                                                                                                                                                                |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


