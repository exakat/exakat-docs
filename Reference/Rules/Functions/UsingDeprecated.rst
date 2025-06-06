.. _functions-usingdeprecated:


.. _using-deprecated-method:

Using Deprecated Method
+++++++++++++++++++++++

.. meta::
	:description:
		Using Deprecated Method: A call to a deprecated method has been spotted.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Using Deprecated Method
	:twitter:description: Using Deprecated Method: A call to a deprecated method has been spotted
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Using Deprecated Method
	:og:type: article
	:og:description: A call to a deprecated method has been spotted
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Using Deprecated Method.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UsingDeprecated.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/UsingDeprecated.html","name":"Using Deprecated Method","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"A call to a deprecated method has been spotted","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Using Deprecated Method.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

A call to a deprecated method has been spotted. A method is deprecated when it bears a ``@deprecated`` parameter in its typehint definition.

Deprecated methods which are not called are not reported.

.. code-block:: php
   
   <?php
   
   // not deprecated method
   not_deprecated();
   
   // deprecated methods
   deprecated();
   $object = new X();
   $object->deprecatedToo();
   
   /**
    * @deprecated since version 2.0.0
    */
   function deprecated() {}
   
   // PHP 8.0 attribute for deprecation
   class X {
       #[ Deprecated]
       function deprecatedToo() {}
   }
   
   function not_deprecated() {}
   
   ?>

See also `@deprecated <https://docs.phpdoc.org/latest/references/phpdoc/tags/deprecated.html>`_.

Connex PHP features
-------------------

  + `Deprecated <https://php-dictionary.readthedocs.io/en/latest/dictionary/deprecated.ini.html>`_


Suggestions
___________

* Replace the deprecated call with a stable call
* Remove the deprecated attribute from the method definition
* Remove the deprecated call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UsingDeprecated                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Attributes <ruleset-Attributes>`                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


