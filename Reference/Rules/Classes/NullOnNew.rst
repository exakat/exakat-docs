.. _classes-nullonnew:

.. _null-on-new:

Null On New
+++++++++++

.. meta::
	:description:
		Null On New: Until PHP 7, some classes instantiation could yield null, instead of throwing an exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Null On New
	:twitter:description: Null On New: Until PHP 7, some classes instantiation could yield null, instead of throwing an exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Null On New
	:og:type: article
	:og:description: Until PHP 7, some classes instantiation could yield null, instead of throwing an exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Null On New.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NullOnNew.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Classes\/NullOnNew.html","name":"Null On New","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Until PHP 7, some classes instantiation could yield null, instead of throwing an exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Null On New.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Until PHP 7, some classes instantiation could yield null, instead of throwing an `exception <https://www.php.net/exception>`_. 

After issuing a 'new' with those classes, it was important to check if the returned object were null or not. No `exception <https://www.php.net/exception>`_ were thrown.
This inconsistency has been cleaned in PHP 7 : see See `Internal Constructor Behavior <https://wiki.php.net/rfc/internal_constructor_behaviour>`_

.. code-block:: php
   
   <?php
   
   // Example extracted from the wiki below
   $mf = new MessageFormatter('en_US', '{this was made intentionally incorrect}');
   if ($mf === null) {
       echo 'Surprise!';
   }
   
   ?>

See also `PHP RFC: Constructor behaviour of internal classes <https://wiki.php.net/rfc/internal_constructor_behaviour>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_
  + `new <https://php-dictionary.readthedocs.io/en/latest/dictionary/new.ini.html>`_
  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Suggestions
___________

* Remove the check on null after a new instantiation




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/NullOnNew                                                                                                                                                                                                                                                                                            |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>`, :ref:`CompatibilityPHP55 <ruleset-CompatibilityPHP55>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                                                                                                                                                                                                       |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                                                                                                        |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                                                                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                                                                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


