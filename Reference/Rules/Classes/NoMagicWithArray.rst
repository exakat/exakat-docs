.. _classes-nomagicwitharray:


.. _no-magic-method-with-array:

No Magic Method With Array
++++++++++++++++++++++++++


.. meta::

	:description:

		No Magic Method With Array: Magic method ``__set()`` doesn't work for array syntax.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No Magic Method With Array

	:twitter:description: No Magic Method With Array: Magic method ``__set()`` doesn't work for array syntax

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No Magic Method With Array

	:og:type: article

	:og:description: Magic method ``__set()`` doesn't work for array syntax

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Magic Method With Array.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoMagicWithArray.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NoMagicWithArray.html","name":"No Magic Method With Array","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"Magic method ``__set()`` doesn't work for array syntax","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Magic Method With Array.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Magic method ``__set()`` doesn't work for array syntax. 

When overloading properties, they can only be used for scalar values, excluding arrays. Under the hood, PHP uses ``__get()`` to reach for the name of the property, and doesn't recognize the following index as an array. It yields an `error <https://www.php.net/error>`_ : "Indirect modification of overloaded property".



It is possible to use the array syntax with a magic property : by making the ``__get`` returns an array, the syntax will actually extract the expected item in the array.

This is not reported by linting.

In this analysis, only properties that are found to be magic are reported. For example, using the b property outside the class scope is not reported, as it would yield too many false-positives.

.. code-block:: php
   
   <?php
   
   class c {
       private $a;
       private $o = array();
   
       function __get($name) {
           return $this->o[$name];
       }
       
       function foo() {
           // property b doesn't exists
           $this->b['a'] = 3;
           
           print_r($this);
       }
   
       // This method has no impact on the issue
       function __set($name, $value) {
           $this->o[$name] = $value;
       }
   }
   
   $c = new c();
   $c->foo();
   
   ?>

See also `Overload <https://www.php.net/manual/en/language.oop5.overloading.php#object.get>`_.

Related PHP errors 
-------------------

  + `Indirect modification of overloaded property %s::$%s has no effect <https://php-errors.readthedocs.io/en/latest/messages/indirect-modification-of-overloaded-property-%25s%3A%3A%24%25s-has-no-effect.html>`_



Connex PHP features
-------------------

  + `magic-method <https://php-dictionary.readthedocs.io/en/latest/dictionary/magic-method.ini.html>`_


Suggestions
___________

* Use a distinct method to append a new value to that property
* Assign the whole array, and not just one of its elements




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NoMagicWithArray                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`LintButWontExec <ruleset-LintButWontExec>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                                                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Note         | This issue may lint but will not run                                                                                                                                                                                           |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


