.. _traits-traitusage:

.. _traits-usage:

Traits Usage
++++++++++++

.. meta::
	:description:
		Traits Usage: This is the list of traits that are actually 'used' in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Traits Usage
	:twitter:description: Traits Usage: This is the list of traits that are actually 'used' in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Traits Usage
	:og:type: article
	:og:description: This is the list of traits that are actually 'used' in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Traits Usage.html
	:og:locale: en
This is the list of traits that are actually 'used' in the code. There are classes or traits that 'use' them. Traits can only be accessed by calling them with the 'use' command. It is not possible to reach a trait element (method, constant, property) by refering to them with the trait name, even for `static <https://www.php.net/manual/en/language.oop5.static.php>`_ elements: the code must go through the host class.

.. code-block:: php
   
   <?php
   
   trait t {
       function t() {
           echo 'I\'m in t';
       }
   }
   
   class foo {
       use t;
   }
   
   $x = new foo();
   $x->t();
   
   ?>

See also `Traits <https://www.php.net/manual/en/language.oop5.traits.php>`_.

Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/TraitUsage                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


