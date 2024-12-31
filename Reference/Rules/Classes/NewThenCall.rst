.. _classes-newthencall:

.. _new-object-then-immediate-call:

New Object Then Immediate Call
++++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		New Object Then Immediate Call: This rule reports immediate calls on a new object.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: New Object Then Immediate Call
	:twitter:description: New Object Then Immediate Call: This rule reports immediate calls on a new object
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: New Object Then Immediate Call
	:og:type: article
	:og:description: This rule reports immediate calls on a new object
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/NewThenCall.html
	:og:locale: en
  This rule reports immediate calls on a new object. This can be simplified with a parenthesis structure, including with the assignation inside the parenthesis.

It is also being discussed to drop the parenthesis altogether. 


.. code-block:: php
   
   <?php
   
   $a = new Foo();
   $a->bar();
   
   ($a = new Foo())->bar();
   
   ?>

See also `new MyClass()->method() without parentheses <https://twitter.com/pronskiy/status/1739646806407999653>`_.


Suggestions
___________

* Condense the two expressions into one




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NewThenCall                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Class Review <ruleset-Class-Review>`                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


