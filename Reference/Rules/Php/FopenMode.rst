.. _php-fopenmode:


.. _wrong-fopen()-mode:

Wrong fopen() Mode
++++++++++++++++++

.. meta::
	:description:
		Wrong fopen() Mode: Wrong file opening for fopen().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong fopen() Mode
	:twitter:description: Wrong fopen() Mode: Wrong file opening for fopen()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong fopen() Mode
	:og:type: article
	:og:description: Wrong file opening for fopen()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong fopen() Mode.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/FopenMode.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/FopenMode.html","name":"Wrong fopen() Mode","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Wrong file opening for fopen()","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong fopen() Mode.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Wrong file opening for `fopen() <https://www.php.net/fopen>`_.

`fopen() <https://www.php.net/fopen>`_ has a few modes, as described in the documentation : 'r', 'r+', for reading;  'w', 'w+' for writing; 'a', 'a+' for appending; 'x', 'x+' for modifying; 'c', 'c+' for writing and locking, 't' for text files and windows only.
An optional 'b' may be used to make the `fopen() <https://www.php.net/fopen>`_ call more portable and binary safe. Another optional 't' may be used to make the `fopen() <https://www.php.net/fopen>`_ call process automatically text input : this one should be avoided. 
Any other values are not understood by PHP.

.. code-block:: php
   
   <?php
   
   // open the file for reading, in binary mode
   $fp = fopen('/tmp/php.txt', 'rb');
   
   // New option e in PHP 7.0.16 and 7.1.2 (beware of compatibility)
   $fp = fopen('/tmp/php.txt', 'rbe');
   
   // Unknown option x
   $fp = fopen('/tmp/php.txt', 'rbx');
   
   ?>
Related PHP errors 
-------------------

  + `Failed to open stream: `+wr' is not a valid mode for fopen <https://php-errors.readthedocs.io/en/latest/messages/%60%25s%27-is-not-a-valid-mode-for-fopen.html>`_



Connex PHP features
-------------------

  + `File Mode <https://php-dictionary.readthedocs.io/en/latest/dictionary/file-mode.ini.html>`_


Suggestions
___________

* Check the docs, choose the right opening mode.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/FopenMode                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-tikiwiki-php-fopenmode`, :ref:`case-humo-gen-php-fopenmode`                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


