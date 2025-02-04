.. _classes-shouldhavedestructor:


.. _should-have-destructor:

Should Have Destructor
++++++++++++++++++++++

.. meta::
	:description:
		Should Have Destructor: PHP destructors are called when the object is being destroyed.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Have Destructor
	:twitter:description: Should Have Destructor: PHP destructors are called when the object is being destroyed
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Have Destructor
	:og:type: article
	:og:description: PHP destructors are called when the object is being destroyed
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Have Destructor.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldHaveDestructor.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ShouldHaveDestructor.html","name":"Should Have Destructor","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"PHP destructors are called when the object is being destroyed","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Have Destructor.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP destructors are called when the object is being destroyed. By default, PHP calls recursively the destructor on internal objects, until everything is unset.

Unsetting objects and resources explicitly in the destructor is a good practice to reduce the amount of memory in use. It helps PHP resource counter to keep the numbers low, and easier to clean. This is a major advantage for long running scripts.

Unsetting scalar properties, such as `string` or `int` is not necessary, as they are stored independently and cleaned automatically by PHP. Closing resources of type `resource` is important : there might be some final calls to close it cleanly. Unsetting an object only decreases the reference count for that object : it is still available to other objects that kept it as property.

Destructor is useful for long-running resources : file resource, sockets, a file lock or persistent database connexion. This is a good time to finish cleanly, and close.

Internally to the application, destructors are also useful with `static <https://www.php.net/manual/en/language.oop5.static.php>`_ properties and registries : for example, the current class may deregister from a list of listener, so that this list is still up to date. Otherwise, the registry keeps the object alive.

.. code-block:: php
   
   <?php
   
   class x {
       function __construct() {
           $this->p = new y();
       }
   
       function __destruct() {
           print __METHOD__.PHP_EOL;
           unset($this->p);
       }
   }
   
   class y {
       function __construct() {
           print __METHOD__.PHP_EOL;
           $this->p = new y();
       }
   
       function __destruct() {
           print __METHOD__.PHP_EOL;
           unset($this->p);
       }
   }
   
   $a = (new x);
   sleep(1);
   
   // This increment the resource counter by one for the property.
   $p = $a->p;
   unset($a);
   sleep(3);
   
   print 'end'.PHP_EOL;
   // Y destructor is only called here, as the object still exists in $p.
   
   ?>

See also `Destructor <https://www.php.net/manual/en/language.oop5.decon.php#language.oop5.decon.destructor>`_ and `Php Destructors <https://stackoverflow.com/questions/3566155/php-destructors>`_.

Connex PHP features
-------------------

  + `Destructor <https://php-dictionary.readthedocs.io/en/latest/dictionary/destructor.ini.html>`_


Suggestions
___________

* Add a destruct method to the class to help clean at destruction time.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ShouldHaveDestructor                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.4                                                                                                                   |
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


