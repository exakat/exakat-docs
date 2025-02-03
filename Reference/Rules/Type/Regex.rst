.. _type-regex:


.. _regex-inventory:

Regex Inventory
+++++++++++++++


.. meta::

	:description:

		Regex Inventory: All regular expressions used in the code.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Regex Inventory

	:twitter:description: Regex Inventory: All regular expressions used in the code

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Regex Inventory

	:og:type: article

	:og:description: All regular expressions used in the code

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Regex Inventory.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Regex.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Type\/Regex.html","name":"Regex Inventory","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 14 Jan 2025 12:52:58 +0000","dateModified":"Tue, 14 Jan 2025 12:52:58 +0000","description":"All regular expressions used in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Regex Inventory.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

All regular expressions used in the code. PHP relies on the PCRE extension to process them, with the functions `preg_match() <https://www.php.net/preg_match>`_, `preg_replace() <https://www.php.net/preg_replace>`_, etc. 
``mbstring`` regular expressions are also collected. POSIX regex are not listed : they were deprecated in PHP 7.0.

.. code-block:: php
   
   <?php
   
   // PCRE regex used with preg_match
   preg_match('/[abc]+/', $string);
   
   // Mbstring regex, in the arabic range
   if(mb_ereg('[\x{0600}-\x{06FF}]', $text))
   
   ?>

See also `preg_match() <https://www.php.net/preg_match>`_, `ext/mbstring <http://www.php.net/manual/en/book.mbstring.php> `_ and `ext/pcre <http://www.php.net/manual/en/book.pcre.php> `_.

Related PHP errors 
-------------------

  + `No ending delimiter '/' <https://php-errors.readthedocs.io/en/latest/messages/no-ending-delimiter-%27%25c%27-found.html>`_



Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Regex                                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.14                                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


