.. _classes-couldbereadonly:

.. _class-could-be-readonly:

Class Could Be Readonly
+++++++++++++++++++++++

.. meta::
	:description:
		Class Could Be Readonly: When all properties are readonly, it is possible to set the option at the class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Could Be Readonly
	:twitter:description: Class Could Be Readonly: When all properties are readonly, it is possible to set the option at the class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Could Be Readonly
	:og:type: article
	:og:description: When all properties are readonly, it is possible to set the option at the class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Could Be Readonly.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeReadonly.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/CouldBeReadonly.html","name":"Class Could Be Readonly","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When all properties are readonly, it is possible to set the option at the class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Could Be Readonly.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When all properties are readonly, it is possible to set the option at the class. This feature was introduced in PHP 8.2.

.. code-block:: php
   
   <?php
   
   // This class could be readonly
   class x {
   	private readonly A $p;
   	private readonly A $p2;
   }
   
   ?>

See also `PHP 8.2: readonly Classes <https://php.watch/versions/8.2/readonly-classes>`_.

Connex PHP features
-------------------

  + `readonly <https://php-dictionary.readthedocs.io/en/latest/dictionary/readonly.ini.html>`_


Suggestions
___________

* Remove readonly from the properties, and add it to the classes.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/CouldBeReadonly                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.1                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and more recent                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------+


