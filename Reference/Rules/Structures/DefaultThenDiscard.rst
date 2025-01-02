.. _structures-defaultthendiscard:

.. _default-then-discard:

Default Then Discard
++++++++++++++++++++

.. meta::
	:description:
		Default Then Discard: Discard the value before assigning it.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Default Then Discard
	:twitter:description: Default Then Discard: Discard the value before assigning it
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Default Then Discard
	:og:type: article
	:og:description: Discard the value before assigning it
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Default Then Discard.html
	:og:locale: en
Discard the value before assigning it. 

In the code below, the variable is assigned a default value. Then, this value is immediately tested and discarded. 

It is more readable to test the value, and discard it, or assign it later, rather than assign first then discard it later.

.. code-block:: php
   
   <?php
   
   $a = $a ?? null;
   if ($a === null) {
   	throw new Exception();
   }
   doSomething();
   
   // Alternative code
   
   if (!isset($a) || $a === null) {
   	throw new Exception();
   }
   // $a has a valid value for the purpose
   
   doSomething();
   
   ?>
Connex PHP features
-------------------

  + `default <https://php-dictionary.readthedocs.io/en/latest/dictionary/default.ini.html>`_


Suggestions
___________

* Test the value and bail out if it is not valid before assigning it




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DefaultThenDiscard                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


