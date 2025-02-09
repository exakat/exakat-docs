.. _structures-unreachablecode:


.. _unreachable-code:

Unreachable Code
++++++++++++++++

.. meta::
	:description:
		Unreachable Code: Code may be unreachable, because other instructions prevent its reaching.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unreachable Code
	:twitter:description: Unreachable Code: Code may be unreachable, because other instructions prevent its reaching
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unreachable Code
	:og:type: article
	:og:description: Code may be unreachable, because other instructions prevent its reaching
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unreachable Code.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnreachableCode.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UnreachableCode.html","name":"Unreachable Code","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Code may be unreachable, because other instructions prevent its reaching","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unreachable Code.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Code may be unreachable, because other instructions prevent its reaching. 

For example, it be located after throw, return, `exit() <https://www.www.php.net/exit>`_, `die() <https://www.php.net/die>`_, goto, `break <https://www.php.net/manual/en/control-structures.break.php>`_ or `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ : this way, it cannot be reached, as the previous instruction will divert the `engine <https://www.php.net/engine>`_ to another part of the code. 



This is dead code, that may be removed.

.. code-block:: php
   
   <?php
   
   function foo() {
       $a++;
       return $a;
       $b++;      // $b++ can't be reached;
   }
   
   function bar() {
       if ($a) {
           return $a;
       } else {
           return $b;
       }
       $b++;      // $b++ can't be reached;
   }
   
   foreach($a as $b) {
       $c += $b;
       if ($c > 10) {
           continue 1;
       } else {
           $c--;
           continue;
       }
       $d += $e;   // this can't be reached
   }
   
   $a = 1;
   goto B;
   class foo {}    // Definitions are accessible, but not functioncalls
   B: 
   echo $a;
   
   ?>

See also `Unreachable code <https://en.wikipedia.org/wiki/Unreachable_code>`_.

Connex PHP features
-------------------

  + `Unreachable Code <https://php-dictionary.readthedocs.io/en/latest/dictionary/unreachable-code.ini.html>`_


Suggestions
___________

* Remove the unreachable code
* Remove the blocking expression, and let the rest of the code execute




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UnreachableCode                                                                                                                                   |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Dead code <ruleset-Dead-code>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| ClearPHP     | `no-dead-code <https://github.com/dseguy/clearPHP/tree/master/rules/no-dead-code.md>`__                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+


