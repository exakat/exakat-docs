.. _structures-mbstringunknownencoding:


.. _mbstring-unknown-encoding:

Mbstring Unknown Encoding
+++++++++++++++++++++++++

.. meta::
	:description:
		Mbstring Unknown Encoding: The encoding used is not known to the ext/mbstring extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mbstring Unknown Encoding
	:twitter:description: Mbstring Unknown Encoding: The encoding used is not known to the ext/mbstring extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mbstring Unknown Encoding
	:og:type: article
	:og:description: The encoding used is not known to the ext/mbstring extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mbstring Unknown Encoding.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MbstringUnknownEncoding.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MbstringUnknownEncoding.html","name":"Mbstring Unknown Encoding","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"The encoding used is not known to the ext\/mbstring extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mbstring Unknown Encoding.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

The encoding used is not known to the ext/mbstring extension.

This analysis takes in charge all ``mbstring`` encoding and aliases. The full list of supported mbstring encoding is available with `mb_list_encodings() <https://www.php.net/mb_list_encodings>`_. Each encoding alias is available with `mb_encoding_aliases() <https://www.php.net/mb_encoding_aliases>`_.

.. code-block:: php
   
   <?php
   
   // Invalid encoding
   $str = mb_strtolower($str, 'utf_8');
   
   // Valid encoding
   $str = mb_strtolower($str, 'utf8');
   $str = mb_strtolower($str, 'UTF8');
   $str = mb_strtolower($str, 'UTF-8');
   
   ?>

See also `ext/mbstring <http://www.php.net/manual/en/book.mbstring.php>`_.

Connex PHP features
-------------------

  + `Encoding <https://php-dictionary.readthedocs.io/en/latest/dictionary/encoding.ini.html>`_
  + `Multibyte String <https://php-dictionary.readthedocs.io/en/latest/dictionary/mbstring.ini.html>`_


Suggestions
___________

* Use a valid mbstring encoding




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MbstringUnknownEncoding                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


