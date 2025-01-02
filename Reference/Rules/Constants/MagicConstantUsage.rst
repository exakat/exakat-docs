.. _constants-magicconstantusage:

.. _magic-constant-usage:

Magic Constant Usage
++++++++++++++++++++

.. meta::
	:description:
		Magic Constant Usage: There are eight magical constants that change depending on where they are used.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Magic Constant Usage
	:twitter:description: Magic Constant Usage: There are eight magical constants that change depending on where they are used
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Magic Constant Usage
	:og:type: article
	:og:description: There are eight magical constants that change depending on where they are used
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Magic Constant Usage.html
	:og:locale: en
There are eight magical constants that change depending on where they are used. For example, the value of ``__LINE__`` depends on the line that it's used on in your script. These special constants are case-insensitive.

+ ``__LINE__``
+ ``__FILE__``
+ ``__DIR__``
+ ``__FUNCTION__``
+ ``__CLASS__``
+ ``__TRAIT__``
+ ``__METHOD__``
+ ``__NAMESPACE__``



.. code-block:: php
   
   <?php
   
   echo 'This code is in file '__FILE__.', line '.__LINE__;
   
   ?>

See also `Magic Constants <https://www.php.net/manual/en/language.constants.predefined.php>`_.

Connex PHP features
-------------------

  + `magic-constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-constant.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/MagicConstantUsage                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
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


