.. _classes-classusage:


.. _class-usage:

Class Usage
+++++++++++

.. meta::
	:description:
		Class Usage: List of classes in use in the code source.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Class Usage
	:twitter:description: Class Usage: List of classes in use in the code source
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Class Usage
	:og:type: article
	:og:description: List of classes in use in the code source
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Class Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/ClassUsage.html","name":"Class Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"List of classes in use in the code source","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Class Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

List of classes in use in the code source.

.. code-block:: php
   
   <?php
   
   // Class may be used in a use expression
   use MyClass as MyAliasedClass;
   
   // class may be aliased with class_alias
   class_alias('MyOtherAliasedClass', 'MyClass');
   
   // Class may be instanciated
   $o = new MyClass();
   
   // Class may be used with instanceof
   var_dump($o instanceof \MyClass);
   
   // Class may be used in static calls
   MyClass::aConstant;
   echo MyClass::$aProperty;
   echo MyClass::aMethod( $o );
   
   // Class may be extended
   class MyOtherClass {
   
   }
   
   class MyClass extends MyOtherClass {
       const aConstant = 1;
       
       public static $aProperty = 2;
       
       // also used as a typehint
       public static function aMethod(MyClass $object) {
           return __METHOD__;
       }
   }
   
   ?>
Connex PHP features
-------------------

  + `Class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/ClassUsage                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


