.. _complete-setclonelink:


.. _set-clone-link:

Set Clone Link
++++++++++++++

.. meta::
	:description:
		Set Clone Link: This command creates a link DEFINITION between a clone call, and its equivalent magic method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Set Clone Link
	:twitter:description: Set Clone Link: This command creates a link DEFINITION between a clone call, and its equivalent magic method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Set Clone Link
	:og:type: article
	:og:description: This command creates a link DEFINITION between a clone call, and its equivalent magic method
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Set Clone Link.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetCloneLink.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Complete\/SetCloneLink.html","name":"Set Clone Link","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"This command creates a link DEFINITION between a clone call, and its equivalent magic method","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Set Clone Link.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This command creates a link DEFINITION between a clone call, and its equivalent magic method.
This command may not detect all possible link for the clone. It may be missing information about the nature of the clone object.

.. code-block:: php
   
   <?php
   
   class x {
       // Store an object
       private $a;
       
       function foo() {
           // This clone is linked to the magic method below
           return clone $this;
       }
       
       function __clone() {
           $this->a = clone $this->a;
       }
   }
   
   // This is not linked to any __clone method, by lack of information
   clone $x; 
   
   ?>

See also `Object Cloning <https://www.php.net/manual/en/language.oop5.cloning.php>`_.

Connex PHP features
-------------------

  + `clone <https://php-dictionary.readthedocs.io/en/latest/dictionary/clone.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Complete/SetCloneLink                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`NoDoc <ruleset-NoDoc>`              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


