.. _classes-directcalltomagicmethod:


.. _no-direct-call-to-magic-method:

No Direct Call To Magic Method
++++++++++++++++++++++++++++++


.. meta::

	:description:

		No Direct Call To Magic Method: PHP features magic methods, which are methods related to operators.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No Direct Call To Magic Method

	:twitter:description: No Direct Call To Magic Method: PHP features magic methods, which are methods related to operators

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No Direct Call To Magic Method

	:og:type: article

	:og:description: PHP features magic methods, which are methods related to operators

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Direct Call To Magic Method.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DirectCallToMagicMethod.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/DirectCallToMagicMethod.html","name":"No Direct Call To Magic Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"PHP features magic methods, which are methods related to operators","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Direct Call To Magic Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP features magic methods, which are methods related to operators.

Magic methods, such as `__get() <https://www.php.net/manual/en/language.oop5.magic.php>`_, related to =, or `__clone() <https://www.php.net/manual/en/language.oop5.magic.php>`_, related to ``clone``, are supposed to be used in an object environment, and not with direct call. 

It is recommended to use the magic method with its intended usage, and not to call it directly. For example, typecast to ``string`` instead of calling the `__toString() <https://www.php.net/manual/en/language.oop5.magic.php>`_ method.

Accessing those methods in a `static <https://www.php.net/manual/en/language.oop5.static.php>`_ way is also discouraged.

.. code-block:: php
   
   <?php
   // Write
     print $x->a;
   // instead of 
     print $x->__get('a'); 
   
   class Foo {
       private $b = "secret";
   
       public function __toString() {
           return strtoupper($this->b);
       }
   }
   
   $bar = new Foo();
   echo (string) $bar;
   
   ?>

See also `Magical PHP: __call <https://www.garfieldtech.com/blog/magical-php-call>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/DirectCallToMagicMethod                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


