.. _dump-collectblocksize:


.. _collect-block-size:

Collect Block Size
++++++++++++++++++


.. meta::

	:description:

		Collect Block Size: Collect block size for instructions such as for, foreach, while, do.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Collect Block Size

	:twitter:description: Collect Block Size: Collect block size for instructions such as for, foreach, while, do

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Collect Block Size

	:og:type: article

	:og:description: Collect block size for instructions such as for, foreach, while, do

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Collect Block Size.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectBlockSize.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Dump\/CollectBlockSize.html","name":"Collect Block Size","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Collect block size for instructions such as for, foreach, while, do","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Collect Block Size.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Collect block size for instructions such as for, foreach, while, do...while, ifthen.

This is a starting point for reviewing large blocks of code and extract methods.

.. code-block:: php
   
   <?php
   
   foreach($array as $key => $value) {
   	// This is a one line block for the foreach
   	doSomething();
   }
   
   if($a === $b) {
   	$a++;
   	// This is a two lines block for the ifthen
   	doSomething($a, $b);
   }
   
   ?>
Connex PHP features
-------------------

  + `inclusion <https://php-dictionary.readthedocs.io/en/latest/dictionary/inclusion.ini.html>`_
  + `ifthen <https://php-dictionary.readthedocs.io/en/latest/dictionary/ifthen.ini.html>`_
  + `foreach <https://php-dictionary.readthedocs.io/en/latest/dictionary/foreach.ini.html>`_
  + `while <https://php-dictionary.readthedocs.io/en/latest/dictionary/while.ini.html>`_
  + `dowhile <https://php-dictionary.readthedocs.io/en/latest/dictionary/dowhile.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Dump/CollectBlockSize                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dump <ruleset-Dump>`                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
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


