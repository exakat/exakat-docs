.. _structures-mbstringnonencodings:


.. _mbstring-unknown-encodings:

Mbstring Unknown Encodings
++++++++++++++++++++++++++

.. meta::
	:description:
		Mbstring Unknown Encodings: mbstring functions require one of its supported encoding as parameter.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mbstring Unknown Encodings
	:twitter:description: Mbstring Unknown Encodings: mbstring functions require one of its supported encoding as parameter
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mbstring Unknown Encodings
	:og:type: article
	:og:description: mbstring functions require one of its supported encoding as parameter
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mbstring Unknown Encodings.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MbStringNonEncodings.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/MbStringNonEncodings.html","name":"Mbstring Unknown Encodings","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Thu, 16 Jan 2025 17:40:16 +0000","dateModified":"Thu, 16 Jan 2025 17:40:16 +0000","description":"mbstring functions require one of its supported encoding as parameter","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Mbstring Unknown Encodings.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

mbstring functions require one of its supported encoding as parameter. 

For example, `mb_chr() <https://www.php.net/mb_chr>`_ requires encoding as second parameter. The supported encodings are available with `mb_list_encodings() <https://www.php.net/mb_list_encodings>`_ and `mb_encoding_aliases() <https://www.php.net/mb_encoding_aliases>`_.

A wrong encoding generates a fatal `error <https://www.php.net/error>`_.

Here are some of the dropped encodings, depending on PHP versions: 

+ PHP 7.0
  	+ auto
+ PHP 8.0
  	+ pass
+ PHP 8.1
    + wchar
    + byte2be
    + byte2le
    + byte4be
    + byte4le
    + jis-ms
    + cp50220raw
+ PHP 8.2
  	+ qprint
  	+ base64
  	+ uuencode
  	+ html-entities

.. code-block:: php
   
   <?php
   
   	print mb_chr(128024, 'UTF-8')); // emoji of an elephant
   
   	//Argument #2 ($encoding) must be a valid encoding, "elephpant" given 
   	print mb_chr($value, 'elephpant')); 
   }
   ?>
Related PHP errors 
-------------------

  + `Argument #2 ($encoding) must be a valid encoding, "%s" given <https://php-errors.readthedocs.io/en/latest/messages/must-be-a-valid-encoding%2C-%22%25s%22-given.html>`_



Connex PHP features
-------------------

  + `Multibyte String <https://php-dictionary.readthedocs.io/en/latest/dictionary/mbstring.ini.html>`_
  + `Encoding <https://php-dictionary.readthedocs.io/en/latest/dictionary/encoding.ini.html>`_


Suggestions
___________

* Use a valid encoding for the PHP version.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MbStringNonEncodings                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


