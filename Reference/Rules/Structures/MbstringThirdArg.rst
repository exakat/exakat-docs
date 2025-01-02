.. _structures-mbstringthirdarg:

.. _mbstring-third-arg:

Mbstring Third Arg
++++++++++++++++++

.. meta::
	:description:
		Mbstring Third Arg: Some mbstring functions use the third argument for offset, not for encoding.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mbstring Third Arg
	:twitter:description: Mbstring Third Arg: Some mbstring functions use the third argument for offset, not for encoding
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mbstring Third Arg
	:og:type: article
	:og:description: Some mbstring functions use the third argument for offset, not for encoding
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mbstring Third Arg.html
	:og:locale: en
Some mbstring functions use the third argument for offset, not for encoding.

Those are the following functions : 

* `mb_strrichr() <https://www.php.net/mb_strrichr>`_
* `mb_stripos() <https://www.php.net/mb_stripos>`_
* `mb_strrpos() <https://www.php.net/mb_strrpos>`_
* `mb_strstr() <https://www.php.net/mb_strstr>`_
* `mb_stristr() <https://www.php.net/mb_stristr>`_
* `mb_strpos() <https://www.php.net/mb_strpos>`_
* `mb_strripos() <https://www.php.net/mb_strripos>`_
* `mb_strrchr() <https://www.php.net/mb_strrchr>`_
* `mb_strrichr() <https://www.php.net/mb_strrichr>`_
* `mb_substr() <https://www.php.net/mb_substr>`_

.. code-block:: php
   
   <?php
   
   // Display BC
   echo mb_substr('ABC', 1 , 2, 'UTF8');
   
   // Yields Warning: mb_substr() expects parameter 3 to be int, string given
   // Display 0 (aka, substring from 0, for length (int) 'UTF8' => 0)
   echo mb_substr('ABC', 1 ,'UTF8');
   
   ?>
Connex PHP features
-------------------

  + `mbstring <https://php-dictionary.readthedocs.io/en/latest/dictionary/mbstring.ini.html>`_


Suggestions
___________

* Add a third argument
* Use the default encoding (aka, omit both third AND fourth argument)




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/MbstringThirdArg                                                                                                                                                             |
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
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


