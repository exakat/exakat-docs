.. _structures-onlyfirstbyte:

.. _only-first-byte-:

Only First Byte 
++++++++++++++++

.. meta::
	:description:
		Only First Byte : When assigning a char to a string with an array notation, only the first byte is used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Only First Byte 
	:twitter:description: Only First Byte : When assigning a char to a string with an array notation, only the first byte is used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Only First Byte 
	:og:type: article
	:og:description: When assigning a char to a string with an array notation, only the first byte is used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Only First Byte .html
	:og:locale: en
When assigning a char to a string with an array notation, only the first byte is used.

.. code-block:: php
   
   <?php
       $str = 'xy';  
   
       // first letter is now a
       $str[0] = 'a';
   
       // second letter is now b, c is ignored
       $str[1] = 'bc';
   ?>

See also `String access and modification by character <https://www.php.net/manual/en/language.types.string.php#language.types.string.substr>`_.

Related PHP errors 
-------------------

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Only+the+first+byte+will+be+assigned+to+the+string+offset.html>`_




Suggestions
___________

* Remove extra bytes when assigning to a string
* Use concatenation
* Use strpos() and substr() functions
* Use explode(), implode() functions and array manipulations




Specs
_____

+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/OnlyFirstByte                                                                                                |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.2                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | All                                                                                                                     |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                   |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                         |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.0                                                                                                                 |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                    |
+------------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+------------------+-------------------------------------------------------------------------------------------------------------------------+


