.. _attributes-friend:


.. _friend-attribute:

Friend Attribute
++++++++++++++++

.. meta::
	:description:
		Friend Attribute: A method or class can supply via a #[Friend] attribute a list of classes.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Friend Attribute
	:twitter:description: Friend Attribute: A method or class can supply via a #[Friend] attribute a list of classes
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Friend Attribute
	:og:type: article
	:og:description: A method or class can supply via a #[Friend] attribute a list of classes
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Friend Attribute.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/Friend.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Attributes\/Friend.html","name":"Friend Attribute","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 21 Jan 2025 08:40:17 +0000","dateModified":"Tue, 21 Jan 2025 08:40:17 +0000","description":"A method or class can supply via a #[Friend] attribute a list of classes","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Friend Attribute.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A method or class can supply via a #[Friend] `attribute <https://www.php.net/attribute>`_ a list of classes. Only these classes can call the method. This is loosely based on the C++ friend feature.

+ Multiple classes can be specified. E.g. #[Friend(Foo\:\:class, Bar\:\:class)]
+ A class can have a #[Friend] `attribute <https://www.php.net/attribute>`_, classes listed here are applied to every method.
+ The #[Friend] `attribute <https://www.php.net/attribute>`_ is additive. If a class and a method have the #[Friend] the method can be called from any of the classes listed. E.g.
+ This is is currently limited to method calls (including `__construct) <https://www.php.net/manual/en/language.oop5.decon.php>`_.

+ The `Attribute <https://www.php.net/attribute>`_ is limited to the exact classes, the family hierarchy is not searched.
+ Multiple attributes can be specified to add more classes. E.g. #[Friend(Foo\:\:class)] #[Friend(Bar\:\:class)]

Based on the specificiations from Dave Liddament.

.. code-block:: php
   
   <?php
   
   class Person
   {
       #[Friend(PersonBuilder::class)]
       public function __construct()
       {
           // Some implementation
       }
   }
   
   class PersonBuilder
   {
       public function build(): Person
       {
           $person = new Person(): // OK as PersonBuilder is allowed to call Person's construct method.
           // set up Person
           return $person;
       }
   }
   
   // ERROR Call to Person::__construct is not from PersonBuilder
   $person = new Person();
   
   ?>

See also `Friend <https://github.com/DaveLiddament/php-language-extensions#friend>`_ and `php-language-extension <https://github.com/DaveLiddament/php-language-extensions>`_.

Connex PHP features
-------------------

  + `Attribute <https://php-dictionary.readthedocs.io/en/latest/dictionary/attribute.ini.html>`_


Suggestions
___________

* Add the reported classes as friend to the original class
* Remove the call to the class from the reported classes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Attributes/Friend                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Attributes <ruleset-Attributes>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


