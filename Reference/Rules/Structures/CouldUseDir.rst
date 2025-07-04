.. _structures-couldusedir:


.. _could-use-\_\_dir\_\_:

Could Use __DIR__
+++++++++++++++++

.. meta::
	:description:
		Could Use __DIR__: Use __DIR__ constant to access the current file's parent directory.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use __DIR__
	:twitter:description: Could Use __DIR__: Use __DIR__ constant to access the current file's parent directory
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use __DIR__
	:og:type: article
	:og:description: Use __DIR__ constant to access the current file's parent directory
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use __DIR__.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseDir.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CouldUseDir.html","name":"Could Use __DIR__","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use __DIR__ constant to access the current file's parent directory","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use __DIR__.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use `__DIR__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ constant to access the current file's `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ `directory <https://www.php.net/directory>`_. 

Avoid using `dirname() <https://www.php.net/dirname>`_ on `__FILE__ <https://www.php.net/manual/en/language.constants.predefined.php>`_.
`__DIR__ <https://www.php.net/manual/en/language.constants.predefined.php>`_ has been introduced in PHP 5.3.0.

.. code-block:: php
   
   <?php
   
   // Better way
   $fp = fopen(__DIR__.'/myfile.txt', 'r');
   
   // compatible, but slow way
   $fp = fopen(dirname(__FILE__).'/myfile.txt', 'r');
   
   // Since PHP 5.3
   assert(dirname(__FILE__) == __DIR__);
   
   ?>

See also `Magic Constants <https://www.php.net/manual/en/language.constants.predefined.php>`_.

Connex PHP features
-------------------

  + `Magic Constants <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-constant.ini.html>`_


Suggestions
___________

* Use __DIR__ instead of ``dirname(__FILE__);``




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CouldUseDir                                                                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`, :ref:`php-cs-fixable <ruleset-php-cs-fixable>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-structures-couldusedir`, :ref:`case-piwigo-structures-couldusedir`                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


