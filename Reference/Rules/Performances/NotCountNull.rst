.. _performances-notcountnull:

.. _no-count-with-0:

No Count With 0
+++++++++++++++

.. meta::
	:description:
		No Count With 0: Comparing count(), strlen() or mb_strlen() to 0 is a waste of resources.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: No Count With 0
	:twitter:description: No Count With 0: Comparing count(), strlen() or mb_strlen() to 0 is a waste of resources
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: No Count With 0
	:og:type: article
	:og:description: Comparing count(), strlen() or mb_strlen() to 0 is a waste of resources
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Count With 0.html
	:og:locale: en
Comparing `count() <https://www.php.net/count>`_, `strlen() <https://www.php.net/strlen>`_ or `mb_strlen() <https://www.php.net/mb_strlen>`_ to 0 is a waste of resources. There are three distinct situations.

When comparing `count() <https://www.php.net/count>`_ with 0, with ===, ==, !==, !=, it is more efficient to use empty(). empty() is a language construct that checks if a value is present, while `count() <https://www.php.net/count>`_ actually load the number of element.
When comparing `count() <https://www.php.net/count>`_ strictly with 0 and ``>``, it is more efficient to use ``!(empty(  ))``
Comparing `count() <https://www.php.net/count>`_, `strlen() <https://www.php.net/strlen>`_ or `mb_strlen() <https://www.php.net/mb_strlen>`_ with other values than 0 cannot be replaced with a comparison with empty().

Note that this is a micro-optimisation : since PHP keeps track of the number of elements in arrays (or number of chars in strings), the total computing time of both operations is often lower than a ms. However, both functions tends to be heavily used, and may even be used inside loops.

.. code-block:: php
   
   <?php
   
   // Checking if an array is empty
   if (count($array) == 0) {
       // doSomething();
   }
   // This may be replaced with 
   if (empty($array)) {
       // doSomething();
   }
   
   ?>

See also `count <https://www.php.net/count>`_, `strlen <https://www.php.net/strlen>`_ and `mb_strlen <https://www.php.net/mb_strlen>`_.

Connex PHP features
-------------------

  + `count <https://php-dictionary.readthedocs.io/en/latest/dictionary/count.ini.html>`_


Suggestions
___________

* Use empty() on the data
* Compare the variable with a default value, such as an empty array




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/NotCountNull                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-contao-performances-notcountnull`, :ref:`case-wordpress-performances-notcountnull`                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


