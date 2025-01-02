.. _structures-multipleunset:

.. _multiple-unset():

Multiple Unset()
++++++++++++++++

.. meta::
	:description:
		Multiple Unset(): Unset() accepts multiple arguments, unsetting them one after each other.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Multiple Unset()
	:twitter:description: Multiple Unset(): Unset() accepts multiple arguments, unsetting them one after each other
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Multiple Unset()
	:og:type: article
	:og:description: Unset() accepts multiple arguments, unsetting them one after each other
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Multiple Unset().html
	:og:locale: en
Unset() accepts multiple arguments, unsetting them one after each other. It is more efficient to call unset() once, than multiple times.

.. code-block:: php
   
   <?php
   
   // One call to unset only
   unset($a, $b, $c, $d);
   
   // Too many calls to unset
   unset($a);
   unset($b);
   unset($c);
   unset($d);
   
   ?>

See also `unset <https://www.php.net/unset>`_.

Connex PHP features
-------------------

  + `unset <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Merge all unset into one call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MultipleUnset                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                   |
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


