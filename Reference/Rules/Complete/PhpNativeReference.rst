.. _complete-phpnativereference:


.. _php-native-reference-variable:

Php Native Reference Variable
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Php Native Reference Variable: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Php Native Reference Variable

	:twitter:description: Php Native Reference Variable: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Php Native Reference Variable

	:og:type: article

	:og:description: Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php Native Reference Variable.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/PhpNativeReference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/PhpNativeReference.html","name":"Php Native Reference Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Native functions, such as sort() (first argument), or preg_match_all() (third argument), use reference","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Php Native Reference Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Native functions, such as `sort() <https://www.php.net/sort>`_ (first argument), or `preg_match_all() <https://www.php.net/preg_match_all>`_ (third argument), use reference.

.. code-block:: php
   
   <?php
   
   $a = [3,1,2];
   sort($a);
   $a === [1,2,3];
   
   ?>
Connex PHP features
-------------------

  + `reference <https://php-dictionary.readthedocs.io/en/latest/dictionary/reference.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/PhpNativeReference                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


