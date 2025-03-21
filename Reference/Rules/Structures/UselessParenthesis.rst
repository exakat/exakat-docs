.. _structures-uselessparenthesis:


.. _useless-parenthesis:

Useless Parenthesis
+++++++++++++++++++

.. meta::
	:description:
		Useless Parenthesis: Situations where parenthesis are not necessary, and may be removed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Useless Parenthesis
	:twitter:description: Useless Parenthesis: Situations where parenthesis are not necessary, and may be removed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Useless Parenthesis
	:og:type: article
	:og:description: Situations where parenthesis are not necessary, and may be removed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Useless Parenthesis.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessParenthesis.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UselessParenthesis.html","name":"Useless Parenthesis","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Situations where parenthesis are not necessary, and may be removed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Useless Parenthesis.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Situations where parenthesis are not necessary, and may be removed.

Parenthesis group several elements together, and allows for a more readable expression. They are used with logical and mathematical expressions. They are necessary when the precedence of the operators are not the intended execution order : for example, when an addition must be performed before the multiplication.

Sometimes, the parenthesis provide the same execution order than the default order : they are deemed useless, from the PHP point of view. Yet, they may add readability to the code. In special circumstances, they may also protect the code from evolution in the precedence of operators : for example, ``1 + 2 . '.' . 3 + 4;`` has different results between PHP 8 and PHP 7.

.. code-block:: php
   
   <?php
   
       if ( ($condition) ) {}
       while( ($condition) ) {}
       do $a++; while ( ($condition) );
       
       switch ( ($a) ) {}
       $y = (1);
       ($y) == (1);
       
       f(($x));
   
       // = has precedence over == 
       ($a = $b) == $c;
       
       ($a++);
       
       // No need for parenthesis in default values
       function foo($c = ( 1 + 2) ) {}
   ?>

See also `Operators Precedence <https://www.php.net/manual/en/language.operators.precedence.php>`_.

Connex PHP features
-------------------

  + `Operators <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator.ini.html>`_
  + `Operator Precedence <https://php-dictionary.readthedocs.io/en/latest/dictionary/operator-precedence.ini.html>`_


Suggestions
___________

* Remove useless parenthesis, unless they are important for readability.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UselessParenthesis                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-mautic-structures-uselessparenthesis`, :ref:`case-woocommerce-structures-uselessparenthesis`                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


