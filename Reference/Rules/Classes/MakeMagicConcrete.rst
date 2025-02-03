.. _classes-makemagicconcrete:

.. _make-magic-concrete:

Make Magic Concrete
+++++++++++++++++++

.. meta::
	:description:
		Make Magic Concrete: Speed up execution by replacing magic calls by concrete properties.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Make Magic Concrete
	:twitter:description: Make Magic Concrete: Speed up execution by replacing magic calls by concrete properties
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Make Magic Concrete
	:og:type: article
	:og:description: Speed up execution by replacing magic calls by concrete properties
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Make Magic Concrete.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MakeMagicConcrete.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/MakeMagicConcrete.html","name":"Make Magic Concrete","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Speed up execution by replacing magic calls by concrete properties","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Make Magic Concrete.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Speed up execution by replacing magic calls by concrete properties. 

Magic properties are managed dynamically, with `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_ and `__set() <https://www.php.net/manual/en/language.oop5.magic.php>`_. They replace property access by a methodcall, and they are much slower than the first. 

When a property name is getting used more often, it is worth creating a concrete property, and skip the method call. The threshold for ``magicMemberUsage`` is 1, by default.

.. code-block:: php
   
   <?php
   
   class x {
       private $values = array('a' => 1,
                               'b' => 2);
                               
       function __get($name) {
           return $this->values[$name] ?? '';
       }
   }
   
   $x = new x();
   // Access to 'a' is repeated in the code, at least 'magicMemberUsage' time (cf configuration below)
   echo $x->a; 
   
   ?>

+------------------+---------+---------+---------------------------------------------------------------------------------------+
| Name             | Default | Type    | Description                                                                           |
+------------------+---------+---------+---------------------------------------------------------------------------------------+
| magicMemberUsage | 1       | integer | Minimal number of magic member usage across the code, to trigger a concrete property. |
+------------------+---------+---------+---------------------------------------------------------------------------------------+



See also :ref:`Memoize MagicCall <memoize-magiccall>`.

Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Make frequently used properties concrete; keep the highly dynamic as magic




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/MakeMagicConcrete                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.3                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


