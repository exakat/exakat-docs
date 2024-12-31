.. _functions-identity:

.. _identity:

Identity
++++++++

.. meta\:\:
	:description:
		Identity: This method, function or closure returns one of its argument, without modification.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Identity
	:twitter:description: Identity: This method, function or closure returns one of its argument, without modification
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Identity
	:og:type: article
	:og:description: This method, function or closure returns one of its argument, without modification
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/Identity.html
	:og:locale: en
  This method, function or `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ returns one of its argument, without modification. This is the identity function, which might not be called at all, as it does nothing but return the same incoming argument. It might also be ready for future use.

.. code-block:: php
   
   <?php
   
   function foo($a) {
       return $a;
   }
   
   ?>
Connex PHP features
-------------------

  + `identity <https://php-dictionary.readthedocs.io/en/latest/dictionary/identity.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/Identity                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


