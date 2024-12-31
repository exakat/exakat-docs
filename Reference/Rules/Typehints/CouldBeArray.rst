.. _typehints-couldbearray:

.. _could-be-array-typehint:

Could Be Array Typehint
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Could Be Array Typehint: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar typehint.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Array Typehint
	:twitter:description: Could Be Array Typehint: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar typehint
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Array Typehint
	:og:type: article
	:og:description: This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar typehint
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Typehints/CouldBeArray.html
	:og:locale: en
  This rule spots arguments, class constants, properties or return values that may be labeled with the ``array`` scalar typehint. 

.. code-block:: php
   
   <?php
   
   // $arg is used as an array in this function, so it may be typed : array
   functions foo($arg) {
   
       // the returned value is always an array, so this function might be typed as : array
       return array($arg[3]);
   }
   
   ?>

See also `Type declarations  <https://www.php.net/manual/en/functions.arguments.php#functions.arguments.type-declaration>`_.

Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Add `array` typehint to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeArray                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


