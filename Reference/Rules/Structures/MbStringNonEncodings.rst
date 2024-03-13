.. _structures-mbstringnonencodings:

.. _mbstring-unknown-encodings:

Mbstring Unknown Encodings
++++++++++++++++++++++++++

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
| Features     | mbstring, encoding                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


