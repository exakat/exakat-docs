.. _classes-overwrittenconst:


.. _overwritten-class-constants:

Overwritten Class Constants
+++++++++++++++++++++++++++

.. meta::
	:description:
		Overwritten Class Constants: Those class constants are overwriting  a parent class's constant.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Class Constants
	:twitter:description: Overwritten Class Constants: Those class constants are overwriting  a parent class's constant
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Class Constants
	:og:type: article
	:og:description: Those class constants are overwriting  a parent class's constant
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Class Constants.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/OverwrittenConst.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/OverwrittenConst.html","name":"Overwritten Class Constants","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Wed, 05 Mar 2025 15:10:46 +0000","dateModified":"Wed, 05 Mar 2025 15:10:46 +0000","description":"Those class constants are overwriting  a parent class's constant","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overwritten Class Constants.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Those class constants are overwriting  a `parent <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ class's constant. This may lead to confusion, as the value of the constant may change depending on the way it is called.

.. code-block:: php
   
   <?php
   
   class foo {
       const C = 1;
   }
   
   class bar extends foo {
       const C = 2;
       
       function x() {
           // depending on the access to C, value is different.
           print self::C.' '.static::C.' '.parent::C;
       }
   }
   
   ?>
Related PHP errors 
-------------------

  + `Cannot inherit previously-inherited or override constant A from interface i <https://php-errors.readthedocs.io/en/latest/messages/cannot-inherit-previously-inherited-or-override-constant-%25s-from-interface-%25s.html>`_
  + `%s %s inherits both %s::%s and %s::%s <https://php-errors.readthedocs.io/en/latest/messages/%25s-%25s-inherits-both-%25s%3A%3A%25s-and-%25s%3A%3A%25s.html>`_



Connex PHP features
-------------------

  + `Static Constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/class-constant.ini.html>`_
  + `Overwrite <https://php-dictionary.readthedocs.io/en/latest/dictionary/overwrite.ini.html>`_


Suggestions
___________

* Remove the constant in the interface
* Remove the constant in the class
* Rename one of the constants




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/OverwrittenConst                                                                                                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


