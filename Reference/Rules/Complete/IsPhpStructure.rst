.. _complete-isphpstructure:

.. _is-php-structure:

Is PHP Structure
++++++++++++++++

.. meta::
	:description:
		Is PHP Structure: This rules marks atoms with ``isPhp``, as part of the standard PHP elements.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is PHP Structure
	:twitter:description: Is PHP Structure: This rules marks atoms with ``isPhp``, as part of the standard PHP elements
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is PHP Structure
	:og:type: article
	:og:description: This rules marks atoms with ``isPhp``, as part of the standard PHP elements
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is PHP Structure.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/IsPhpStructure.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/IsPhpStructure.html","name":"Is PHP Structure","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This rules marks atoms with ``isPhp``, as part of the standard PHP elements","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Is PHP Structure.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This rules marks atoms with ``isPhp``, as part of the standard PHP elements. For example, ``Datetime``, ``E_ALL``, etc. This `attribute <https://www.php.net/attribute>`_ is available in the `engine <https://www.php.net/engine>`_, but not displayed.

.. code-block:: php
   
   <?php
   
   // strtolower is marked as isPhp 
   $string = strtolower($s) . foo($s);
   
   ?>

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/IsPhpStructure                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.6                                                                                                                   |
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


