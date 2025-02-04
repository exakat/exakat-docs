.. _classes-classaliasusage:


.. _usage-of-class\_alias():

Usage Of class_alias()
++++++++++++++++++++++

.. meta::
	:description:
		Usage Of class_alias(): ``class_alias`` creates dynamically an alias for classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Usage Of class_alias()
	:twitter:description: Usage Of class_alias(): ``class_alias`` creates dynamically an alias for classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Usage Of class_alias()
	:og:type: article
	:og:description: ``class_alias`` creates dynamically an alias for classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Usage Of class_alias().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassAliasUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassAliasUsage.html","name":"Usage Of class_alias()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"``class_alias`` creates dynamically an alias for classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Usage Of class_alias().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``class_alias`` creates dynamically an alias for classes.

.. code-block:: php
   
   <?php
   
   class foo { }
   
   class_alias('foo', 'bar');
   
   $a = new foo;
   $b = new bar;
   
   // the objects are the same
   var_dump($a == $b, $a === $b);
   var_dump($a instanceof $b);
   
   // the classes are the same
   var_dump($a instanceof foo);
   var_dump($a instanceof bar);
   
   var_dump($b instanceof foo);
   var_dump($b instanceof bar);
   
   ?>

See also `class_alias <https://www.php.net/class_alias>`_.

Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `Class Aliases <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-alias.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassAliasUsage                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


