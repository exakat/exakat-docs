.. _classes-shoulduseself:


.. _could-use-self:

Could Use self
++++++++++++++

.. meta::
	:description:
		Could Use self: ``self`` keyword refers to the current class, or any of its parents.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Could Use self
	:twitter:description: Could Use self: ``self`` keyword refers to the current class, or any of its parents
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Could Use self
	:og:type: article
	:og:description: ``self`` keyword refers to the current class, or any of its parents
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Could Use self.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldUseSelf.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldUseSelf.html","name":"Could Use self","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"``self`` keyword refers to the current class, or any of its parents","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Could Use self.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``self`` keyword refers to the current class, or any of its parents. Using it is just as fast as the full class name, it is as readable and it is will not be changed upon class or namespace change.

It is also routinely used in traits : there, ``self`` represents the class in which the trait is used, or the trait itself.

.. code-block:: php
   
   <?php
   
   class x {
       const FOO = 1;
       
       public function bar() {
           return self::FOO;
   // same as return x::FOO;
       }
   }
   
   ?>

See also `Scope Resolution Operator (::) <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_.

Connex PHP features
-------------------

  + `Self <https://php-dictionary.readthedocs.io/en/latest/dictionary/self.ini.html>`_
  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Replace the explicit name with ``self``




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ShouldUseSelf                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Class Review <ruleset-Class-Review>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                                 |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-wordpress-classes-shoulduseself`, :ref:`case-livezilla-classes-shoulduseself`                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


