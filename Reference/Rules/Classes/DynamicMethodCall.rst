.. _classes-dynamicmethodcall:


.. _dynamic-methodcall:

Dynamic Methodcall
++++++++++++++++++

.. meta::
	:description:
		Dynamic Methodcall: Dynamic calls to class methods.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Methodcall
	:twitter:description: Dynamic Methodcall: Dynamic calls to class methods
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Methodcall
	:og:type: article
	:og:description: Dynamic calls to class methods
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Methodcall.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicMethodCall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DynamicMethodCall.html","name":"Dynamic Methodcall","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Dynamic calls to class methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dynamic Methodcall.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Dynamic calls to class methods.

.. code-block:: php
   
   <?php
   
   class x {
       static public function foo() {}
              public function bar() {}
   }
   
   $staticmethod = 'foo';
   // dynamic static method call to x::foo()
   x::$staticmethod();
   
   $method = 'bar';
   // dynamic method call to bar()
   $object = new x();
   $object->$method();
   
   ?>
Connex PHP features
-------------------

  + `Dynamic Call <https://php-dictionary.readthedocs.io/en/latest/dictionary/dynamic-call.ini.html>`_
  + `Method <https://php-dictionary.readthedocs.io/en/latest/dictionary/method.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DynamicMethodCall                                                                                                                                                               |
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


