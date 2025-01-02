.. _typehints-couldbeint:

.. _type-could-be-integer:

Type Could Be Integer
+++++++++++++++++++++

.. meta::
	:description:
		Type Could Be Integer: This rule marks arguments, class constants, properties and return types that can be set to the integer type ``int``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Type Could Be Integer
	:twitter:description: Type Could Be Integer: This rule marks arguments, class constants, properties and return types that can be set to the integer type ``int``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Type Could Be Integer
	:og:type: article
	:og:description: This rule marks arguments, class constants, properties and return types that can be set to the integer type ``int``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Type Could Be Integer.html
	:og:locale: en
This rule marks arguments, class constants, properties and return types that can be set to the integer type ``int``.

.. code-block:: php
   
   <?php
   
   // Accept an int as input 
   function foo($b) {
       // Returns an int
       return $b + 8;
   }
   
   ?>
Connex PHP features
-------------------

  + `integer <https://php-dictionary.readthedocs.io/en/latest/dictionary/integer.ini.html>`_
  + `type <https://php-dictionary.readthedocs.io/en/latest/dictionary/type.ini.html>`_


Suggestions
___________

* Add `int` typehint to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeInt                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Typechecks <ruleset-Typechecks>`                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


