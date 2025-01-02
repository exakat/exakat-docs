.. _typehints-couldbenever:

.. _type-could-be-never:

Type Could Be Never
+++++++++++++++++++

.. meta::
	:description:
		Type Could Be Never: Mark return types that can be set to ``never``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Type Could Be Never
	:twitter:description: Type Could Be Never: Mark return types that can be set to ``never``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Type Could Be Never
	:og:type: article
	:og:description: Mark return types that can be set to ``never``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Type Could Be Never.html
	:og:locale: en
Mark return types that can be set to ``never``.

.. code-block:: php
   
   <?php
   
   function foo($b) {
       // this function never returns
       die();
   }
   
   ?>
Connex PHP features
-------------------

  + `never <https://php-dictionary.readthedocs.io/en/latest/dictionary/never.ini.html>`_


Suggestions
___________

* Add the 'never' returntype




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeNever                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Typechecks <ruleset-Typechecks>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.1 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


