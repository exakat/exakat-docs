.. _structures-heredocdelimiterfavorite:

.. _heredoc-delimiter:

Heredoc Delimiter
+++++++++++++++++

  Heredoc and Nowdoc expressions may use a variety of delimiters. 

There seems to be a standard delimiter in the code, and some exceptions : one or several forms are dominant (> 90%), while the others are rare. 

The analyzed code has less than 10% of the rare delimiters. For consistency reasons, it is recommended to make them all the same. 

Generally, one or two delimiters are used, with generic value. It is recommended to use a humanly readable delimiter : SQL, HTML, XML, GREMLIN, etc. This helps readability in the code.


.. code-block:: php
   
   <?php
   
   echo <<<SQL
   SELECT * FROM table1;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table2;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table3;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table4;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table5;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table11;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table12;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table13;
   SQL;
   
   // Nowdoc
   echo <<<'SQL'
   SELECT * FROM table14;
   SQL;
   
   echo <<<SQL
   SELECT * FROM table15;
   SQL;
   
   
   echo <<<HEREDOC
   SELECT * FROM table215;
   HEREDOC;
   
   ?>

Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/HeredocDelimiterFavorite                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Coding conventions <ruleset-Coding-conventions>`, :ref:`Preferences <ruleset-Preferences>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                        |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Features     | heredoc                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_    |
+--------------+----------------------------------------------------------------------------------------------------------------------------+


