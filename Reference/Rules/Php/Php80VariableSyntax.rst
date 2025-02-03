.. _php-php80variablesyntax:


.. _php-8.0-variable-syntax-tweaks:

Php 8.0 Variable Syntax Tweaks
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Php 8.0 Variable Syntax Tweaks: Several variable syntaxes are added in version 8.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Php 8.0 Variable Syntax Tweaks
	:twitter:description: Php 8.0 Variable Syntax Tweaks: Several variable syntaxes are added in version 8
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Php 8.0 Variable Syntax Tweaks
	:og:type: article
	:og:description: Several variable syntaxes are added in version 8
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Php 8.0 Variable Syntax Tweaks.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80VariableSyntax.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/Php80VariableSyntax.html","name":"Php 8.0 Variable Syntax Tweaks","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Several variable syntaxes are added in version 8","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Php 8.0 Variable Syntax Tweaks.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Several variable syntaxes are added in version 8.0. They extends the PHP 7.0 syntax updates, and fix a number of edges cases.

In particular, ``new``and ``instanceof`` now support a way to inline the expression, rather than use a temporary variable.

Magic constants are now accessible with array notation, just like another constant. It is also possible to use method calls : although this is Syntacticly correct for PHP, this won't be executed, as the left operand is a string, and not an object.

.. code-block:: php
   
   <?php
   
    // array name is dynamically build
    echo "foo$bar"[0];
    // static method
    "foo$bar"::baz();
    // static property 
    "foo$bar"::$baz;
    
    // Syntactly correct, but not executable
    "foo$bar"->baz();
    
    // expressions with instanceof and new
       $object = new ("class_".$name);
       $x instanceof ("class_$name");
   
       // PHP 7.0 style
       $className = "class_".$name;
       $object = new $className;
   
   ?>

See also `PHP RFC: Variable Syntax Tweaks <https://wiki.php.net/rfc/variable_syntax_tweaks>`_ and `scalar_objects in PHP <https://github.com/nikic/scalar_objects>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_


Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/Php80VariableSyntax                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.0.8                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                                                                                                   |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                      |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


