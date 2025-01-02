.. _classes-undeclaredstaticproperty:

.. _wrong-access-style-to-property:

Wrong Access Style to Property
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Access Style to Property: Use the right syntax when reaching for a property.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Access Style to Property
	:twitter:description: Wrong Access Style to Property: Use the right syntax when reaching for a property
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Access Style to Property
	:og:type: article
	:og:description: Use the right syntax when reaching for a property
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Access Style to Property.html
	:og:locale: en
Use the right syntax when reaching for a property. `Static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties use the ``\:\:`` operator, and non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties use ``->``. 

Mistaking one of the other raise two different reactions from PHP : ``Access to undeclared `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property`` is a fatal `error <https://www.php.net/error>`_, while ``PHP Notice:  Accessing `static <https://www.php.net/manual/en/language.oop5.static.php>`_ property aa\:\:$a as non `static <https://www.php.net/manual/en/language.oop5.static.php>`_`` is a notice.

This analysis reports both `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties with a `->` access, and non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties with a `\:\:` access.

.. code-block:: php
   
   <?php
   
   class a { 
       static public $a = 1;
       
       function foo() {
           echo self::$a; // right
           echo $this->a; // WRONG
       }
   }
   
   class b { 
       public $b = 1;
   
       function foo() {
           echo $this->$b;  // right
           echo b::$b;      // WRONG
       }
   }
   
   ?>

See also `Static Keyword <https://www.php.net/manual/en/language.oop5.static.php>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Accessing+static+property+aa%3A%3A%24a+as+non+static.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/Access+to+undeclared+static+property.html>`_



Connex PHP features
-------------------

  + `declaration <https://php-dictionary.readthedocs.io/en/latest/dictionary/declaration.ini.html>`_


Suggestions
___________

* Match the property call with the definition
* Make the property static




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UndeclaredStaticProperty                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Class Review <ruleset-Class-Review>`                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-humo-gen-classes-undeclaredstaticproperty`                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


