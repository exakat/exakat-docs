.. _classes-noreadonlyassignationinglobal:

.. _no-readonly-assignation-in-global:

No Readonly Assignation In Global
+++++++++++++++++++++++++++++++++

.. meta::
	:description:
		No Readonly Assignation In Global: When a property is marked readonly, it may only be assigned within the class of definition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Readonly Assignation In Global
	:twitter:description: No Readonly Assignation In Global: When a property is marked readonly, it may only be assigned within the class of definition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Readonly Assignation In Global
	:og:type: article
	:og:description: When a property is marked readonly, it may only be assigned within the class of definition
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/NoReadonlyAssignationInGlobal.html
	:og:locale: en
When a property is marked readonly, it may only be assigned within the class of definition.

It cannot be assigned outside this class, in the global scope. It is also immune to class invasion.

.. code-block:: php
   
   <?php
   
   class x {
       public readonly int $p;
       
       function foo() {
           $this->p -= 1; // OK
           
           $x = new x;
           $x->p = 1;     // Not OK, even if $x is of type x
       }
   }
   
   $x = new x;
   $x->p = 1;     // Not OK
   
   ?>
Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+initialize+readonly+property+x%3A%3A%24p+from+global+scope.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Cannot+initialize+readonly+property+x%3A%3A%24p+from+scope+y.html>`_



Connex PHP features
-------------------

  + `readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_
  + `class-invasion <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-invasion.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoReadonlyAssignationInGlobal                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------+


