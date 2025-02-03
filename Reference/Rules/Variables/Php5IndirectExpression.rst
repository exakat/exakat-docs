.. _variables-php5indirectexpression:


.. _php5-indirect-variable-expression:

PHP5 Indirect Variable Expression
+++++++++++++++++++++++++++++++++


.. meta::

	:description:

		PHP5 Indirect Variable Expression: Indirect variable expressions changes between PHP 5 an 7.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: PHP5 Indirect Variable Expression

	:twitter:description: PHP5 Indirect Variable Expression: Indirect variable expressions changes between PHP 5 an 7

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: PHP5 Indirect Variable Expression

	:og:type: article

	:og:description: Indirect variable expressions changes between PHP 5 an 7

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP5 Indirect Variable Expression.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Php5IndirectExpression.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Variables\/Php5IndirectExpression.html","name":"PHP5 Indirect Variable Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Indirect variable expressions changes between PHP 5 an 7","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP5 Indirect Variable Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Indirect variable expressions changes between PHP 5 an 7.

The following structures are evaluated differently in PHP 5 and 7. It is recommended to review them or switch to a less ambiguous syntax.
+-----------------------+-------------------------+-------------------------+
| Expression            | PHP 5 interpretation    | PHP 7 interpretation    |
+-----------------------+-------------------------+-------------------------+
|$$foo['bar']['baz']    |$\{$foo['bar']['baz']\}    |($$foo)['bar']['baz']    |
|$foo->$bar['baz']      |$foo->\{$bar['baz']\}      |($foo->$bar)['baz']      |
|$foo->$bar['baz']()    |$foo->\{$bar['baz']\}()    |($foo->$bar)['baz']()    |
|Foo\:\:$bar['baz']()   |Foo\:\:{$bar['baz']}()   |(Foo\:\:$bar)['baz']()   |
+-----------------------+-------------------------+-------------------------+

.. code-block:: php
   
   <?php
   
   // PHP 7 
   $foo = 'bar';
   $bar['bar']['baz'] = 'foobarbarbaz';
   echo $$foo['bar']['baz'];
   echo ($$foo)['bar']['baz'];
   
   // PHP 5
   $foo['bar']['baz'] = 'bar';
   $bar = 'foobarbazbar';
   echo $$foo['bar']['baz'];
   echo $\{$foo['bar']['baz']\};
   
   ?>

See also `Backward incompatible changes PHP 7.0 <https://www.php.net/manual/en/migration70.incompatible.php>`_.

Connex PHP features
-------------------

  + `global <https://php-dictionary.readthedocs.io/en/latest/dictionary/global.ini.html>`_


Suggestions
___________

* Avoid using complex expressions, mixing ``$$\``, ``[0]`` and ``->`` in the same expression
* Add curly braces \{\} to ensure that the precedence is the same between PHP 5 and 7. For example, ``$$v`` becomes ``$\{$v\}``




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/Php5IndirectExpression                                                                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


