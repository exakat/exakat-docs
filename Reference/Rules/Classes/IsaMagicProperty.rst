.. _classes-isamagicproperty:

.. _is-a-magic-property:

Is A Magic Property
+++++++++++++++++++

.. meta\:\:
	:description:
		Is A Magic Property: Mark properties usage when they are actually a magic call.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is A Magic Property
	:twitter:description: Is A Magic Property: Mark properties usage when they are actually a magic call
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is A Magic Property
	:og:type: article
	:og:description: Mark properties usage when they are actually a magic call
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/IsaMagicProperty.html
	:og:locale: en
  Mark properties usage when they are actually a magic call. 

There is no direct mention of it in the syntax, it has to be checked with the definitions of the class.

.. code-block:: php
   
   <?php
   
   class magicProperty {
       public $b;
       
       function __get($name) {
           // do something with the value
       }
   
       function foo() {
           $this->a;
           $this->b;
       }
   }
   
   ?>

See also `Magic Methods <https://www.php.net/manual/en/language.oop5.magic.php>`_.

Connex PHP features
-------------------

  + `magic-property <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-property.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/IsaMagicProperty                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.17                                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


