.. _classes-usingthisoutsideaclass:


.. _using-$this-outside-a-class:

Using $this Outside A Class
+++++++++++++++++++++++++++

.. meta::
	:description:
		Using $this Outside A Class: ``$this`` is a special variable, that should only be used in a class context.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Using $this Outside A Class
	:twitter:description: Using $this Outside A Class: ``$this`` is a special variable, that should only be used in a class context
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Using $this Outside A Class
	:og:type: article
	:og:description: ``$this`` is a special variable, that should only be used in a class context
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Using $this Outside A Class.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsingThisOutsideAClass.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsingThisOutsideAClass.html","name":"Using $this Outside A Class","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"``$this`` is a special variable, that should only be used in a class context","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Using $this Outside A Class.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``$this`` is a special variable, that should only be used in a class context. 

Until PHP 7.1, ``$this`` may be used as an argument in a function or a method, a global, a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ : while this is legit, it sounds confusing enough to avoid it.
Starting with PHP 7.1, the PHP `engine <https://www.php.net/engine>`_ check thoroughly that ``$this`` is used in an appropriate manner, and raise fatal errors in case it isn't. 

Yet, it is possible to find ``$this`` outside a class : if the file is included inside a class, then ``$this`` will be recognized and validated. If the file is included outside a class context, it will yield a fatal `error <https://www.php.net/error>`_ : ``Using `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ when not in object context``.

.. code-block:: php
   
   <?php
   
   function foo($this) {
       echo $this;
   }
   
   // A closure can be bound to an object at later time. It is valid usage.
   $closure = function ($x) {
       echo $this->foo($x);
   }
   
   ?>

See also `Closure::bind <https://www.php.net/manual/en/closure.bind.php>`_ and `The Basics <https://www.php.net/manual/en/language.oop5.basic.php>`_.

Related PHP errors 
-------------------

  + `Using $this when not in object context <https://php-errors.readthedocs.io/en/latest/messages/using-%24this-when-not-in-object-context.html>`_



Connex PHP features
-------------------

  + `$this <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24this.ini.html>`_


Specs
_____

+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Classes/UsingThisOutsideAClass                                                                                                                                                                                           |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP71 <ruleset-CompatibilityPHP71>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 0.8.4                                                                                                                                                                                                                    |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 7.0 and older                                                                                                                                                                                                   |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Critical                                                                                                                                                                                                                 |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Instant (5 mins)                                                                                                                                                                                                         |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 7.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/thisMustBeInObject.html>`__                                                                                                             |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note             | This issue may lint but will not run                                                                                                                                                                                     |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                  |
+------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


