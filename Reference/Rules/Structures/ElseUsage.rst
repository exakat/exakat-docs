.. _structures-elseusage:


.. _else-usage:

Else Usage
++++++++++


.. meta::

	:description:

		Else Usage: Else can be avoided by various means.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Else Usage

	:twitter:description: Else Usage: Else can be avoided by various means

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Else Usage

	:og:type: article

	:og:description: Else can be avoided by various means

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Else Usage.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ElseUsage.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ElseUsage.html","name":"Else Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Else can be avoided by various means","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Else Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Else can be avoided by various means. 

For example, defaulting values before using a condition; returning early in the method, thus skipping long else blocks; using a ternary operator to assign values conditionnaly. 

Else is the equivalent of the default clause in a switch statement. When the if/then structure can be replaced with a switch can (albeit, a 2-case switch seems strange), then else usage is a good solution.

.. code-block:: php
   
   <?php
   
   // $a is always set
   $a = 'default';
   if ($condition) {
       $a = foo($condition);
   }
   
   // Don't use else for default : set default before
   if ($condition) {
       $a = foo($condition);
   } else {
       $a = 'default';
   }
   
   // Use then to exit 
   if ( ! $condition) {
       return;
   }
   $a = foo($condition);
   
   // don't use else to return
   if ($condition) {
       $a = foo($condition);
   } else {
       return;
   }
   
   ?>

See also `Avoid Else, Return Early <http://blog.timoxley.com/post/47041269194/avoid-else-return-early>`_ and `Why does clean code forbid else expression <https://stackoverflow.com/questions/32677046/why-does-clean-code-forbid-else-expression>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ElseUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
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


