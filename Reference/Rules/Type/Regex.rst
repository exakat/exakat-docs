.. _type-regex:

.. _regex-inventory:

Regex Inventory
+++++++++++++++

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

  + `0 <https://php-errors.readthedocs.io/en/latest/messages/Delimiter+must+not+be+alphanumeric+or+backslash.html>`_
  + `1 <https://php-errors.readthedocs.io/en/latest/messages/No+ending+delimiter+%27%2F%27.html>`_



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


