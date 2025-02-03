.. _typehints-couldbeboolean:

.. _could-be-boolean:

Could Be Boolean
++++++++++++++++

.. meta::
	:description:
		Could Be Boolean: Reports arguments, properties, return types and class constants that can be typed boolean.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Be Boolean
	:twitter:description: Could Be Boolean: Reports arguments, properties, return types and class constants that can be typed boolean
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Be Boolean
	:og:type: article
	:og:description: Reports arguments, properties, return types and class constants that can be typed boolean
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Be Boolean.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeBoolean.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Typehints\/CouldBeBoolean.html","name":"Could Be Boolean","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Reports arguments, properties, return types and class constants that can be typed boolean","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Be Boolean.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Reports arguments, properties, return types and class constants that can be typed boolean.

.. code-block:: php
   
   <?php
   
   // Accept a boolean as input 
   function foo($b) {
       // Returns a boolean
       return $b === true;
   }
   
   ?>

See also `class <https://www.php.net/manual/en/language.oop5.basic.php#language.oop5.basic.class>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Add ``bool`` typehint to the code.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Typehints/CouldBeBoolean                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


