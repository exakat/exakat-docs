.. _classes-usedonceproperty:


.. _used-once-property:

Used Once Property
++++++++++++++++++

.. meta::
	:description:
		Used Once Property: Property used once in their defining class.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Used Once Property
	:twitter:description: Used Once Property: Property used once in their defining class
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Used Once Property
	:og:type: article
	:og:description: Property used once in their defining class
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Used Once Property.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedOnceProperty.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/UsedOnceProperty.html","name":"Used Once Property","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Property used once in their defining class","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Used Once Property.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Property used once in their defining class. 

Properties used in one method only may be used several times, and read only. This may be a class constant. Such properties are meant to be overwritten by an extending class, and that's possible with class constants. 

Setting properties with default values is a good way to avoid littering the code with literal values, and provide a single point of update (by extension, or by hardcoding) for all those situations. A constant is definitely better suited for this task.

.. code-block:: php
   
   <?php
   
   class foo {
       private $defaultCols = '*';
       cont DEFAULT_COLUMNS = '*';
   
       // $this->defaultCols holds a default value. Should be a constant.
       function bar($table, $cols) {
           // This is necessary to activate usage of default values
           if (empty($cols)) {
               $cols = $this->defaultCols;
           }
           $res = $this->query('SELECT '.$cols.' FROM '.$table);
           // ....
       }
   
       // Upgraded version of bar, with default values
       function bar2($table, $cols = self::DEFAULT_COLUMNS) {
           $res = $this->query('SELECT '.$cols.' FROM '.$table);
           // .....
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Suggestions
___________

* Remove the property, as it is probably not unused
* Add another usage of the property where it is useful




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/UsedOnceProperty                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.10.3                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


