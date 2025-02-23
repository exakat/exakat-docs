.. _structures-whilelisteach:


.. _while(list()-=-each()):

While(List() = Each())
++++++++++++++++++++++

.. meta::
	:description:
		While(List() = Each()): This code structure is quite old : it should be replace by the more modern and efficient foreach.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: While(List() = Each())
	:twitter:description: While(List() = Each()): This code structure is quite old : it should be replace by the more modern and efficient foreach
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: While(List() = Each())
	:og:type: article
	:og:description: This code structure is quite old : it should be replace by the more modern and efficient foreach
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/While(List() = Each()).html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WhileListEach.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/WhileListEach.html","name":"While(List() = Each())","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This code structure is quite old : it should be replace by the more modern and efficient foreach","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/While(List() = Each()).html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This code structure is quite old : it should be replace by the more modern and efficient foreach.

This structure is deprecated since PHP 7.2. It may disappear in the future.

.. code-block:: php
   
   <?php
   
       while(list($key, $value) = each($array)) {
           doSomethingWith($key) and $value();
       }
   
       foreach($array as $key => $value) {
           doSomethingWith($key) and $value();
       }
   ?>

See also `PHP RFC: Deprecations for PHP 7.2 : Each() <https://wiki.php.net/rfc/deprecations_php_7_2#each>`_.

Connex PHP features
-------------------

  + `While <https://php-dictionary.readthedocs.io/en/latest/dictionary/while.ini.html>`_


Suggestions
___________

* Change this loop with foreach
* Change this loop with an ``array_*`` functions with a callback




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/WhileListEach                                                                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-openemr-structures-whilelisteach`, :ref:`case-dolphin-structures-whilelisteach`                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


