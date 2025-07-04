.. _php-useclassalias:


.. _use-class\_alias():

Use class_alias()
+++++++++++++++++

.. meta::
	:description:
		Use class_alias(): class_alias() is a PHP features, that allows the creation of class alias, at execution time.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use class_alias()
	:twitter:description: Use class_alias(): class_alias() is a PHP features, that allows the creation of class alias, at execution time
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use class_alias()
	:og:type: article
	:og:description: class_alias() is a PHP features, that allows the creation of class alias, at execution time
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use class_alias().html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseClassAlias.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UseClassAlias.html","name":"Use class_alias()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"class_alias() is a PHP features, that allows the creation of class alias, at execution time","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use class_alias().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`class_alias() <https://www.php.net/class_alias>`_ is a PHP features, that allows the creation of class alias, at execution time. 

Those class aliases are application wide, as they are valid everywhere, yet they have a lower precedence over the use expression. This means that even when a `class_alias() <https://www.php.net/class_alias>`_ was called, the local use expression will have right of execution.

.. code-block:: php
   
   <?php
   
   // static type of aliasing
   use a as c;
   
   class a {}
   class_alias('a', 'b');
   
   new b;
   
   ?>

See also `class_alias <https://www.php.net/class_alias>`_.

Connex PHP features
-------------------

  + `Class Aliases <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-alias.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseClassAlias                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


