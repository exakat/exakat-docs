.. _classes-ambiguousvisibilities:

.. _ambiguous-visibilities:

Ambiguous Visibilities
++++++++++++++++++++++

.. meta\:\:
	:description:
		Ambiguous Visibilities: The properties have the same name, but have different visibilities, across different classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Ambiguous Visibilities
	:twitter:description: Ambiguous Visibilities: The properties have the same name, but have different visibilities, across different classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Ambiguous Visibilities
	:og:type: article
	:og:description: The properties have the same name, but have different visibilities, across different classes
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/AmbiguousVisibilities.html
	:og:locale: en
  The properties have the same name, but have different visibilities, across different classes. 

While it is legit to have a property with the same name in different classes, it may easily lead to confusion. As soon as the context is need to understand if the property is accessible or not, the readability suffers.

It is recommended to handle the same properties in the same way across classes, even when the classes are not related.

.. code-block:: php
   
   <?php
   
   class person {
       public $name;
       private $address;
   }
   
   class gangster {
       private $name;
       public $nickname;
       private $address;
   }
   
   $someone = Human::load(123);
   echo 'Hello, '.$someone->name;
   
   ?>
Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `visibility <https://php-dictionary.readthedocs.io/en/latest/dictionary/visibility.ini.html>`_


Suggestions
___________

* Sync visibilities for both properties, in the different classes
* Use different names for properties with different usages




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AmbiguousVisibilities                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.4                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-typo3-classes-ambiguousvisibilities`                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`missing-visibility`                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


