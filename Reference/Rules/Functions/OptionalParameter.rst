.. _functions-optionalparameter:


.. _optional-parameter:

Optional Parameter
++++++++++++++++++

.. meta::
	:description:
		Optional Parameter: An optional parameter is a method argument that has both a typehint and a default value.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Optional Parameter
	:twitter:description: Optional Parameter: An optional parameter is a method argument that has both a typehint and a default value
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Optional Parameter
	:og:type: article
	:og:description: An optional parameter is a method argument that has both a typehint and a default value
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Optional Parameter.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/OptionalParameter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/OptionalParameter.html","name":"Optional Parameter","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"An optional parameter is a method argument that has both a typehint and a default value","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Optional Parameter.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

An optional parameter is a method argument that has both a typehint and a default value. 

Such argument is optional, as it may be omitted. When this is the case, the code has to differentiate between the default behavior or the actual usage. It is recommended to avoid providing a default value, and use a `null <https://www.php.net/`null <https://www.php.net/null>`_>`_ object.

.. code-block:: php
   
   <?php
       
   class foo {
       function methodWithOptionalArgument(bar $x = null) {
           if ($x === null) {
               // default behavior
           } else {
               // normal behavior
           }
       }
   
       function methodWithCompulsoryArgument(bar $x) {
           // normal behavior
           // $x is always a bar. 
       }
   }
   ?>
Connex PHP features
-------------------

  + `Parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/parameter.ini.html>`_
  + `Optional Parameter <https://php-dictionary.readthedocs.io/en/latest/dictionary/optional-parameter.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/OptionalParameter                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.4                                                                                                                  |
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


