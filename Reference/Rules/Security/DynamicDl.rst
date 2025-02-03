.. _security-dynamicdl:


.. _dynamic-library-loading:

Dynamic Library Loading
+++++++++++++++++++++++

.. meta::
	:description:
		Dynamic Library Loading: Loading a variable dynamically requires a lot of care in the preparation of the library name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Dynamic Library Loading
	:twitter:description: Dynamic Library Loading: Loading a variable dynamically requires a lot of care in the preparation of the library name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Dynamic Library Loading
	:og:type: article
	:og:description: Loading a variable dynamically requires a lot of care in the preparation of the library name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Dynamic Library Loading.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/DynamicDl.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/DynamicDl.html","name":"Dynamic Library Loading","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Loading a variable dynamically requires a lot of care in the preparation of the library name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Dynamic Library Loading.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Loading a variable dynamically requires a lot of care in the preparation of the library name. 

In case of injection in the variable, the dynamic loading of a library gives a lot of power to an intruder.

.. code-block:: php
   
   <?php
   
       // dynamically loading a library
   	dl($library. PHP_SHLIB_SUFFIX);
   
       // dynamically loading ext/vips
   	dl('vips.' . PHP_SHLIB_SUFFIX);
   
       // static loading ext/vips (unix only)
   	dl('vips.so');
   
   ?>

See also `dl <http://www.php.net/dl>`_.

Connex PHP features
-------------------

  + `library-loading <https://php-dictionary.readthedocs.io/en/latest/dictionary/library-loading.ini.html>`_


Suggestions
___________

* Use a switch structure, to make the dl() calls static.
* Avoid using dl() and make the needed extension always available in PHP binary.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/DynamicDl                                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


