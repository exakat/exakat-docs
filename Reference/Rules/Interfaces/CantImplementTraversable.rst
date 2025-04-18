.. _interfaces-cantimplementtraversable:


.. _can't-implement-traversable:

Can't Implement Traversable
+++++++++++++++++++++++++++

.. meta::
	:description:
		Can't Implement Traversable: It is not possible to implement the ``Traversable`` interface directly.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Can't Implement Traversable
	:twitter:description: Can't Implement Traversable: It is not possible to implement the ``Traversable`` interface directly
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Can't Implement Traversable
	:og:type: article
	:og:description: It is not possible to implement the ``Traversable`` interface directly
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Can't Implement Traversable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/CantImplementTraversable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Interfaces\/CantImplementTraversable.html","name":"Can't Implement Traversable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"It is not possible to implement the ``Traversable`` interface directly","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Can't Implement Traversable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

It is not possible to implement the ``Traversable`` interface directly. It is possible to implement it via the ``Iterator`` and ``IteratorAggregate`` classes, which, in turn, implements ``Traversable``.

``Traversable`` may be useful when used with ``instanceof``, ``catch`` or any type specification.

.. code-block:: php
   
   <?php
   
   // This lints, but doesn't run
   class x implements Traversable {
   
   }
   
   if( $argument instanceof Traversable ) {
       // doSomething
   }
   
   ?>

See also `Traversable <https://www.php.net/manual/en/class.traversable.php>`_, `Iterator <https://www.php.net/manual/en/class.iterator.php>`_ and `IteratorAggregate <https://www.php.net/manual/en/class.iteratoraggregate.php>`_.

Related PHP errors 
-------------------

  + `%s %s must implement interface %s as part of either %s or %s <https://php-errors.readthedocs.io/en/latest/messages/%25s-%25s-must-implement-interface-%25s-as-part-of-either-%25s-or-%25s.html>`_
  + `class %s must implement interface %s as part of either %s or %s <https://php-errors.readthedocs.io/en/latest/messages/class-%25s-must-implement-interface-%25s-as-part-of-either-%25s-or-%25s.html>`_



Connex PHP features
-------------------

  + `Interface <https://php-dictionary.readthedocs.io/en/latest/dictionary/interface.ini.html>`_
  + `Throwable <https://php-dictionary.readthedocs.io/en/latest/dictionary/throwable.ini.html>`_


Suggestions
___________

* Extend ``Iterator`` or ``IteratorAggregate``.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Interfaces/CantImplementTraversable                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.8                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


