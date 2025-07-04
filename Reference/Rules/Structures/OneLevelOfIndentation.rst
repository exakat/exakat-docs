.. _structures-onelevelofindentation:


.. _more-than-one-level-of-indentation:

More Than One Level Of Indentation
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		More Than One Level Of Indentation: According to PHP Object Calisthenics, one level of indentation is sufficient.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: More Than One Level Of Indentation
	:twitter:description: More Than One Level Of Indentation: According to PHP Object Calisthenics, one level of indentation is sufficient
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: More Than One Level Of Indentation
	:og:type: article
	:og:description: According to PHP Object Calisthenics, one level of indentation is sufficient
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/More Than One Level Of Indentation.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneLevelOfIndentation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/OneLevelOfIndentation.html","name":"More Than One Level Of Indentation","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"According to PHP Object Calisthenics, one level of indentation is sufficient","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/More Than One Level Of Indentation.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

According to PHP Object Calisthenics, one level of indentation is sufficient.

It helps to abide by the Single Responsibility rule and increase reuse.

.. code-block:: php
   
   <?php
   
   class foo {
       function multipleLevels($array) {
           $return = array();
           foreach($array as $b) {
   
               // This is a second level of indentation
               if ($this->check($b)) { continue; }
               $return[] = $b;
           }
           return $return;
       }
   
       function oneLevel($array) {
           $return = array_filter($array, array($this, 'check'));
           return $return;
       }
   
   }
   
   ?>
Connex PHP features
-------------------

  + `Indentation <https://php-dictionary.readthedocs.io/en/latest/dictionary/indentation.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/OneLevelOfIndentation                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


