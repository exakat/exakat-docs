.. _php-usenullsafeoperator:

.. _use-nullsafe-operator:

Use NullSafe Operator
+++++++++++++++++++++

.. meta::
	:description:
		Use NullSafe Operator: The nullsafe operator ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use NullSafe Operator
	:twitter:description: Use NullSafe Operator: The nullsafe operator ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use NullSafe Operator
	:og:type: article
	:og:description: The nullsafe operator ``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use NullSafe Operator.html
	:og:locale: en
The nullsafe operator ``?->`` is an alternative to the object operator ``->``. It silently fails the whole expression if a null is used for object.

.. code-block:: php
   
   <?php
   
   $o = null;
   
   // PHP 8.0 Failsafe : $r = null;
   $r = $o->method();
   
   // PHP 7.4- : Call to a member function method() on null
   $r = $o->method();
   
   ?>

See also `PHP RFC: Nullsafe operator <https://wiki.php.net/rfc/nullsafe_operator>`_.

Related PHP errors 
-------------------

  + `Call to a member function m() on null <https://php-errors.readthedocs.io/en/latest/messages/call-to-a-member-function-%25s%28%29-on-%25s.html>`_



Connex PHP features
-------------------

  + `object-operator <https://php-dictionary.readthedocs.io/en/latest/dictionary/object-operator.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseNullSafeOperator                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`One Liners <ruleset-One-Liners>`          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.6                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


