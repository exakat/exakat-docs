.. _php-unsetorcast:


.. _unset()-or-(unset):

Unset() Or (unset)
++++++++++++++++++

.. meta::
	:description:
		Unset() Or (unset): Unset() and (unset) have the same functional use.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unset() Or (unset)
	:twitter:description: Unset() Or (unset): Unset() and (unset) have the same functional use
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unset() Or (unset)
	:og:type: article
	:og:description: Unset() and (unset) have the same functional use
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unset() Or (unset).html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UnsetOrCast.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UnsetOrCast.html","name":"Unset() Or (unset)","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Unset() and (unset) have the same functional use","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unset() Or (unset).html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Unset() and (unset) have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that unset() or (unset) are used depending on coding style and files. One file may be consistently using unset(), while the others are all using (unset). 

In PHP 8.0, the cast ``(unset)`` is not available anymore. It is recomended to avoid using it.

.. code-block:: php
   
   <?php
   
   // be consistent
   (unset) $a1;
   (unset) $a2;
   (unset) $a3;
   (unset) $a4;
   (unset) $a5;
   (unset) $a6;
   (unset) $a7;
   (unset) $a8;
   (unset) $a9;
   (unset) $a10;
   (unset) $a11;
   (unset) $a12;
   
   unset($b);
   ?>
Connex PHP features
-------------------

  + `unset <https://php-dictionary.readthedocs.io/en/latest/dictionary/unset.ini.html>`_


Suggestions
___________

* Use the correct parameter name
* Remove all the parameter names from the call
* Create a relay function with the correct parameter names




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UnsetOrCast                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


