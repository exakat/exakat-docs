.. _extensions-extweakref:

.. _ext-weakref:

ext/weakref
+++++++++++

.. meta::
	:description:
		ext/weakref: Weak References for PHP.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/weakref
	:twitter:description: ext/weakref: Weak References for PHP
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/weakref
	:og:type: article
	:og:description: Weak References for PHP
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/weakref.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extweakref.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extweakref.html","name":"ext\/weakref","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Weak References for PHP","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/weakref.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Weak References for PHP.

Weak references provide a non-intrusive gateway to ephemeral objects. Unlike normal (strong) references, weak references do not prevent the garbage collector from freeing that object. For this reason, an object may be destroyed even though a weak reference to that object still exists. In such conditions, the weak reference seamlessly becomes invalid.

.. code-block:: php
   
   <?php
   class MyClass {
       public function __destruct() {
           echo "Destroying object!\n";
       }
   }
   
   $o1 = new MyClass;
   
   $r1 = new WeakRef($o1);
   
   if ($r1->valid()) {
       echo "Object still exists!\n";
       var_dump($r1->get());
   } else {
       echo "Object is dead!\n";
   }
   
   unset($o1);
   
   if ($r1->valid()) {
       echo "Object still exists!\n";
       var_dump($r1->get());
   } else {
       echo "Object is dead!\n";
   }
   ?>

See also `Weak references <https://www.php.net/manual/en/book.weakref.php>`_ and `PECL extension that implements weak references and weak maps in PHP <https://github.com/colder/php-weakref>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extweakref                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


