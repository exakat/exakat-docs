.. _structures-returnvoid:


.. _return-void-:

Return void 
++++++++++++

.. meta::
	:description:
		Return void : Return returns null as default value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Return void 
	:twitter:description: Return void : Return returns null as default value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Return void 
	:og:type: article
	:og:description: Return returns null as default value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Return void .html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ReturnVoid.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ReturnVoid.html","name":"Return void ","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Return returns null as default value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Return void .html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Return returns `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ as default value. It is recommended to mention explicitly '`null <https://www.php.net/`null <https://www.php.net/null>`_>`_' or find a meaningful return such as a boolean or a default value instead.

.. code-block:: php
   
   <?php
   
   function foo(&$a) {
       ++$a;
       // No explicit return : it returns void
   }
   
   function bar(&$a) {
       ++$a;
       
       // Explicit return : it returns null
       return null
   }
   
   ?>

See also `Void functions <https://www.php.net/manual/en/migration71.new-features.php#migration71.new-features.void-functions>`_.

Connex PHP features
-------------------

  + `Void <https://php-dictionary.readthedocs.io/en/latest/dictionary/void.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ReturnVoid                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


