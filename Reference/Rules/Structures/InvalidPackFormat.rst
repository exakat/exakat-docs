.. _structures-invalidpackformat:


.. _invalid-pack-format:

Invalid Pack Format
+++++++++++++++++++

.. meta::
	:description:
		Invalid Pack Format: Some characters are invalid in a pack() format string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Invalid Pack Format
	:twitter:description: Invalid Pack Format: Some characters are invalid in a pack() format string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Invalid Pack Format
	:og:type: article
	:og:description: Some characters are invalid in a pack() format string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Invalid Pack Format.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InvalidPackFormat.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/InvalidPackFormat.html","name":"Invalid Pack Format","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Some characters are invalid in a pack() format string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Invalid Pack Format.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Some characters are invalid in a `pack() <https://www.php.net/pack>`_ format string.

`pack() <https://www.php.net/pack>`_ and `unpack() <https://www.php.net/unpack>`_ accept the following format specifiers : ``aAhHcCsSnviIlLNVqQJPfgGdeExXZ``. 

`unpack() <https://www.php.net/unpack>`_ also accepts a name after the format specifier and an optional quantifier. 

All other situations is not a valid, and produces a warning : ``pack(): Type t: unknown format code``.

Check `pack() <https://www.php.net/pack>`_ documentation for format specifiers that were introduced in various PHP version, namely 7.0, 7.1 and 7.2.

.. code-block:: php
   
   <?php
       $binarydata = pack("nvc*", 0x1234, 0x5678, 65, 66);
       
       // the first unsigned short is stored as 'first'. The next matches are names with numbers.
       $res = unpack('nfirst/vc*', $binarydata);
   ?>

See also `pack <https://www.php.net/pack>`_ and `unpack <https://www.php.net/pack>`_.

Related PHP errors 
-------------------

  + `pack(): Type t: unknown format code <https://php-errors.readthedocs.io/en/latest/messages/type-%25c%3A-unknown-format-code.html>`_
  + `unpack(): Type t: unknown format code <https://php-errors.readthedocs.io/en/latest/messages/type-%25c%3A-unknown-format-code.html>`_



Connex PHP features
-------------------

  + `pack <https://php-dictionary.readthedocs.io/en/latest/dictionary/pack.ini.html>`_


Suggestions
___________

* Fix the packing format with correct values




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/InvalidPackFormat                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.9                                                                                                                                                                                   |
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


