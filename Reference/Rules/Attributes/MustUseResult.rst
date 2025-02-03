.. _attributes-mustuseresult:

.. _mustuseresult:

MustUseResult
+++++++++++++

.. meta::
	:description:
		MustUseResult: The ``MustUseRresult`` attribute means that the returned value of the method must be used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: MustUseResult
	:twitter:description: MustUseResult: The ``MustUseRresult`` attribute means that the returned value of the method must be used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: MustUseResult
	:og:type: article
	:og:description: The ``MustUseRresult`` attribute means that the returned value of the method must be used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/MustUseResult.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MustUseResult.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/MustUseResult.html","name":"MustUseResult","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 23 Jan 2025 14:24:26 +0000","dateModified":"Thu, 23 Jan 2025 14:24:26 +0000","description":"The ``MustUseRresult`` attribute means that the returned value of the method must be used","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/MustUseResult.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>The ``MustUseRresult`` `attribute <https://www.php.net/attribute>`_ means that the returned value of the method must be used. It should at least be collected. 

.. code-block:: php
   
   <?php
   
   class x {
       #[MustUseResult]
       function mustbeused() : int {
           return 1;
       }
       
       function mustnotbeused() : int {
           return 1;
       }
   }
   
   $x = new x;
   
   // Missing usage
   $x->mustbeused();
   
   // Return value is collected, for later usage
   $c = $x->mustbeused();
   
   ?>

See also https://github.com/DaveLiddament/php-language-extensions?tab=readme-ov-file#mustuseresult.

Connex PHP features
-------------------

  + `attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Attributes/MustUseResult                                         |
+--------------+------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>` |
+--------------+------------------------------------------------------------------+
| Exakat since | 2.6.8                                                            |
+--------------+------------------------------------------------------------------+
| PHP Version  | All                                                              |
+--------------+------------------------------------------------------------------+
| Severity     | Minor                                                            |
+--------------+------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                  |
+--------------+------------------------------------------------------------------+
| Precision    | Very high                                                        |
+--------------+------------------------------------------------------------------+
| Related rule | :ref:`must-use-result,-so-it-returns`                            |
+--------------+------------------------------------------------------------------+
| Available in |                                                                  |
+--------------+------------------------------------------------------------------+


