.. _type-heredoc:

.. _heredoc-delimiter-glossary:

Heredoc Delimiter Glossary
++++++++++++++++++++++++++

.. meta\:\:
	:description:
		Heredoc Delimiter Glossary: List of all the delimiters used to build a Heredoc string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Heredoc Delimiter Glossary
	:twitter:description: Heredoc Delimiter Glossary: List of all the delimiters used to build a Heredoc string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Heredoc Delimiter Glossary
	:og:type: article
	:og:description: List of all the delimiters used to build a Heredoc string
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Type/Heredoc.html
	:og:locale: en
  List of all the delimiters used to build a Heredoc string. 

In the example below, ``EOD`` is the delimiter.

.. code-block:: php
   
   <?php
   
   $a = <<<EOD
   heredoc
   EOD;
   
   ?>

See also `Heredoc <https://www.php.net/manual/en/language.types.string.php#language.types.string.syntax.heredoc>`_.

Connex PHP features
-------------------

  + `heredoc <https://php-dictionary.readthedocs.io/en/latest/dictionary/heredoc.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/Heredoc                                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


