.. _structures-deprecatedmbencoding:

.. _deprecated-mb\_string-encodings:

Deprecated Mb_string Encodings
++++++++++++++++++++++++++++++

  Some encodings, available in the mb_string extensions, are deprecated. Starting with PHP 8.2, the following encodings emits a warning: 

+ BASE64
+ UUENCODE
+ HTML-ENTITIES
+ html
+ Quoted-Printable
+ qprint

This applies to the `mb_detect_encoding() <https://www.php.net/mb_detect_encoding>`_ and `mb_convert_encoding() <https://www.php.net/mb_convert_encoding>`_ functions.

.. code-block:: php
   
   <?php
   
   // recommended version
   $base64Encoded = base64_encode('test'));
   
   // Deprecated version
   mb_convert_encoding('test', 'base64'));
   
   ?>

See also `PHP 8.2: Mbstring: Base64, Uuencode, QPrint, and HTML Entity encodings are deprecated <https://php.watch/versions/8.2/mbstring-qprint-base64-uuencode-html-entities-deprecated>`_.


Suggestions
___________

* Use uuencode() and uudecode() functions.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DeprecatedMbEncoding                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP82 <ruleset-CompatibilityPHP82>`                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Features     | encoding                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


