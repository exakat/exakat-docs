.. _extensions-extast:

.. _ext-php-ast:

ext/php-ast
+++++++++++

.. meta::
	:description:
		ext/php-ast: PHP-AST extension (PHP 7.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/php-ast
	:twitter:description: ext/php-ast: PHP-AST extension (PHP 7
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/php-ast
	:og:type: article
	:og:description: PHP-AST extension (PHP 7
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extast.html
	:og:locale: en
PHP-AST extension (PHP 7.0 +).

.. code-block:: php
   
   <?php
   
   $code = <<<'EOC'
   <?php
   $var = 42;
   EOC;
   
   var_dump(ast\parse_code($code, $version=50));
   
   ?>

See also `ext/ast <https://pecl.php.net/package/ast>`_, `Extension exposing PHP 7 abstract syntax tree <https://github.com/nikic/php-ast>`_ and `Introduction of PHP parse and its application in hyperf <https://developpaper.com/introduction-of-php-parse-and-its-application-in-hyperf/>`_.

Connex PHP features
-------------------

  + `ast <https://php-dictionary.readthedocs.io/en/latest/dictionary/ast.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extast                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


