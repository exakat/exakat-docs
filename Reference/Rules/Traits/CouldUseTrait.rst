.. _traits-couldusetrait:

.. _could-use-trait:

Could Use Trait
+++++++++++++++

.. meta::
	:description:
		Could Use Trait: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use Trait
	:twitter:description: Could Use Trait: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use Trait
	:og:type: article
	:og:description: The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use Trait.html
	:og:locale: en
The following classes have been found implementing all of a trait's methods : it could use this trait, and remove duplicated code.

The comparison between the class methods' and the trait's methods are based on token. They may yield some false-positives.

.. code-block:: php
   
   <?php
   
   trait t {
       function t1() {}
       function t2() {}
       function t3() {}
   }
   
   // t1, t2, t3 method could be dropped, and replaced with 'use t'
   class foo1 {
       function t1() {}
       function t2() {}
       function t3() {}
   
       function j() {}
   }
   
   // foo2 is just the same as foo1
   class foo2 {
       use t;
   
       function j() {}
   }
   
   ?>

See also :ref:`Forgotten Interface <forgotten-interface>`.

Connex PHP features
-------------------

  + `trait <https://php-dictionary.readthedocs.io/en/latest/dictionary/trait.ini.html>`_
  + `dry <https://php-dictionary.readthedocs.io/en/latest/dictionary/dry.ini.html>`_
  + `centralization <https://php-dictionary.readthedocs.io/en/latest/dictionary/centralization.ini.html>`_


Suggestions
___________

* Use trait, and remove duplicated code




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Traits/CouldUseTrait                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.5                                                                                                                   |
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


