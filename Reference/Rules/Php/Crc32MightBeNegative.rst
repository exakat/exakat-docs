.. _php-crc32mightbenegative:

.. _crc32()-might-be-negative:

Crc32() Might Be Negative
+++++++++++++++++++++++++

.. meta::
	:description:
		Crc32() Might Be Negative: crc32() may return a negative number, on 32 bits platforms.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Crc32() Might Be Negative
	:twitter:description: Crc32() Might Be Negative: crc32() may return a negative number, on 32 bits platforms
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Crc32() Might Be Negative
	:og:type: article
	:og:description: crc32() may return a negative number, on 32 bits platforms
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/Crc32MightBeNegative.html
	:og:locale: en
`crc32() <https://www.php.net/crc32>`_ may return a negative number, on 32 bits platforms.

According to the manual : Because PHP\'s integer type is signed many ``CRC32`` checksums will `result <https://www.php.net/result>`_ in negative integers on 32 bits platforms. On 64 bits installations, all `crc32() <https://www.php.net/crc32>`_ results will be positive integers though.

.. code-block:: php
   
   <?php
   
   // display the checksum with %u, to make it unsigned
   echo sprintf('%u', crc32($str));
   
   // turn the checksum into an unsigned hexadecimal
   echo dechex(crc32($str));
   
   // avoid concatenating crc32 to a string, as it may be negative on 32bits platforms 
   echo 'prefix'.crc32($str);
   
   ?>

See also `crc32() <https://www.php.net/crc32>`_.

Connex PHP features
-------------------

  + `crc32 <https://php-dictionary.readthedocs.io/en/latest/dictionary/crc32.ini.html>`_


Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Crc32MightBeNegative                                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`PHP recommendations <ruleset-PHP-recommendations>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.0                                                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


