.. _classes-parentfirst:

.. _parent-first:

Parent First
++++++++++++

.. meta::
	:description:
		Parent First: When calling parent constructor, always put it first in the ``__construct`` method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Parent First
	:twitter:description: Parent First: When calling parent constructor, always put it first in the ``__construct`` method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Parent First
	:og:type: article
	:og:description: When calling parent constructor, always put it first in the ``__construct`` method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Parent First.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ParentFirst.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ParentFirst.html","name":"Parent First","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When calling parent constructor, always put it first in the ``__construct`` method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Parent First.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>When calling `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ constructor, always put it first in the ``__construct`` method. 

It ensures the `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ is correctly build before the child start using values. 
This analysis doesn't apply to Exceptions.

.. code-block:: php
   
   <?php
   
   class father {
       protected $name = null;
       
       function __construct() {
           $this->name = init();
       }
   }
   
   class goodSon {
       function __construct() {
           // parent is build immediately, 
           parent::__construct();
           echo "my name is ".$this->name;
       }
   }
   
   class badSon {
       function __construct() {
           // This will fail.
           echo "my name is ".$this->name;
   
           // parent is build later, 
           parent::__construct();
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `parent <https://php-dictionary.readthedocs.io/en/latest/dictionary/parent.ini.html>`_


Suggestions
___________

* Use ``parent::__construct`` as the first call in the constructor.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ParentFirst                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.5                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                    |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-classes-parentfirst`, :ref:`case-prestashop-classes-parentfirst`                                                                     |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                  |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------------+


