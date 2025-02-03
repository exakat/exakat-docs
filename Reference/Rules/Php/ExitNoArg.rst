.. _php-exitnoarg:


.. _exit-without-argument:

Exit Without Argument
+++++++++++++++++++++


.. meta::

	:description:

		Exit Without Argument: This rule reports usage of die and exit without arguments, nor parenthesis.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Exit Without Argument

	:twitter:description: Exit Without Argument: This rule reports usage of die and exit without arguments, nor parenthesis

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Exit Without Argument

	:og:type: article

	:og:description: This rule reports usage of die and exit without arguments, nor parenthesis

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Exit Without Argument.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ExitNoArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ExitNoArg.html","name":"Exit Without Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports usage of die and exit without arguments, nor parenthesis","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Exit Without Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of `die <https://www.php.net/die>`_ and `exit <https://www.www.php.net/exit>`_ without arguments, nor parenthesis. These commands are not functions, and are allowed to be used without parenthesis: by default, they use the 0 status.

.. code-block:: php
   
   <?php
   
   exit; 
   
   die; 
   
   ?>
Connex PHP features
-------------------

  + `exit <https://php-dictionary.readthedocs.io/en/latest/dictionary/exit.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ExitNoArg                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.6                                                                                                                   |
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


