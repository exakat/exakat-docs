.. _structures-regexdelimiter:

.. _regex-delimiter:

Regex Delimiter
+++++++++++++++

  PCRE regular expressions may use a variety of delimiters. 

There seems to be a standard delimiter in the code, and some exceptions : one or several forms are dominant (> 90%), while the others are rare. 

The analyzed code has less than 10% of the rare delimiters. For consistency reasons, it is recommended to make them all the same. 

Generally, one or two delimiters are used, depending on the expected special chars in the scanned strings : for example, / tends to be avoided when parsing HTML.

Regex are literals, or partial literals, used in `preg_match() <https://www.php.net/preg_match>`_, `preg_match_all() <https://www.php.net/preg_match_all>`_, `preg_replace() <https://www.php.net/preg_replace>`_, `preg_replace_callback() <https://www.php.net/preg_replace_callback>`_, `preg_replace_callback_array() <https://www.php.net/preg_replace_callback_array>`_.

.. code-block:: php
   
   <?php
   
   echo 'a';
   echo 'b';
   echo 'c';
   echo 'd';
   echo 'e';
   echo 'f';
   echo 'g';
   echo 'h';
   echo 'i';
   echo 'j';
   echo 'k';
   
   // This should probably be written 'echo';
   print 'l';
   
   ?>

See also `Ideal regex delimiters in PHP <http://codelegance.com/ideal-regex-delimiters-in-php/>`_.

Connex PHP features
-------------------

  + `regex <https://php-dictionary.readthedocs.io/en/latest/dictionary/regex.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/RegexDelimiter                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.5                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


