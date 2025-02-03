.. _attributes-modifyimmutable:


.. _modify-immutable:

Modify Immutable
++++++++++++++++


.. meta::

	:description:

		Modify Immutable: A class, marked as immutable, is being modified.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Modify Immutable

	:twitter:description: Modify Immutable: A class, marked as immutable, is being modified

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Modify Immutable

	:og:type: article

	:og:description: A class, marked as immutable, is being modified

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Modify Immutable.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/ModifyImmutable.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/ModifyImmutable.html","name":"Modify Immutable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"A class, marked as immutable, is being modified","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Modify Immutable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A class, marked as immutable, is being modified. 

This `attribute <https://www.php.net/attribute>`_ is supported as a PHPdoc comment, `@immutable, and as a PHP 8.0 `attribute <https://www.php.net/attribute>`_.

.. code-block:: php
   
   <?php
   
   /** @Immutable */
   #[Immutable]
   class x {
       public $x = 1, $y, $z;
   }
   
   $x = new X;
   // $x->x is modified, while it should not
   $x->x = 2 + $x->z;
   
   // $x->z is read only, as expected
   
   ?>

See also `phpstorm-stubs/meta/attributes/Immutable.php <https://github.com/JetBrains/phpstorm-stubs/blob/master/meta/attributes/Immutable.php>`_ and `PhpStorm 2020.3 EAP \#4: Custom PHP 8 Attributes  <https://blog.jetbrains.com/phpstorm/2020/10/phpstorm-2020-3-eap-4/>`_.

Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Removed the modification
* Clone the immutable object




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/ModifyImmutable                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------+


