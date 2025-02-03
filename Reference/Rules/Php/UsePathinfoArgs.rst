.. _php-usepathinfoargs:


.. _use-pathinfo()-arguments:

Use pathinfo() Arguments
++++++++++++++++++++++++

.. meta::
	:description:
		Use pathinfo() Arguments: pathinfo() has a second argument to select only useful data.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use pathinfo() Arguments
	:twitter:description: Use pathinfo() Arguments: pathinfo() has a second argument to select only useful data
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use pathinfo() Arguments
	:og:type: article
	:og:description: pathinfo() has a second argument to select only useful data
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use pathinfo() Arguments.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsePathinfoArgs.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsePathinfoArgs.html","name":"Use pathinfo() Arguments","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"pathinfo() has a second argument to select only useful data","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use pathinfo() Arguments.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`pathinfo() <https://www.php.net/pathinfo>`_ has a second argument to select only useful data. 

It is twice faster to get only one element from `pathinfo() <https://www.php.net/pathinfo>`_ than get the four of them, and use only one.

This analysis reports `pathinfo() <https://www.php.net/pathinfo>`_ usage, without second argument, where only one or two indices are used, after the call.
Depending on the situation, the functions `dirname() <https://www.php.net/dirname>`_ and `basename() <https://www.php.net/basename>`_ may also be used. They are even faster, when only fetching those data.

.. code-block:: php
   
   <?php
   
   // This could use only PATHINFO_BASENAME
   function foo_db() {
       $a = pathinfo($file2);
       return $a['basename'];
   }
   
   // This could be 2 calls, with PATHINFO_BASENAME and PATHINFO_DIRNAME.
   function foo_de() {
       $a = pathinfo($file3);
       return $a['dirname'].'/'.$a['basename'];
   }
   
   // This is OK : 3 calls to pathinfo() is slower than array access.
   function foo_deb() {
       $a = pathinfo($file4);
       return  $a['dirname'].'/'.$a['filename'].'.'.$a['extension'];
   }
   
   ?>

See also `list <https://www.php.net/manual/en/function.list.php>`_.

Connex PHP features
-------------------

  + `path <https://php-dictionary.readthedocs.io/en/latest/dictionary/path.ini.html>`_


Suggestions
___________

* Use PHP native function pathinfo() and its arguments




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UsePathinfoArgs                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.12                                                                                                                  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                      |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-zend-config-php-usepathinfoargs`, :ref:`case-thinkphp-php-usepathinfoargs`                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


