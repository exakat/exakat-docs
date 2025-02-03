.. _php-usepathinfo:


.. _use-pathinfo:

Use Pathinfo
++++++++++++


.. meta::

	:description:

		Use Pathinfo: Use pathinfo() function instead of string manipulations.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use Pathinfo

	:twitter:description: Use Pathinfo: Use pathinfo() function instead of string manipulations

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use Pathinfo

	:og:type: article

	:og:description: Use pathinfo() function instead of string manipulations

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Pathinfo.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsePathinfo.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/UsePathinfo.html","name":"Use Pathinfo","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Tue, 28 Jan 2025 15:14:39 +0000","dateModified":"Tue, 28 Jan 2025 15:14:39 +0000","description":"Use pathinfo() function instead of string manipulations","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use Pathinfo.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use `pathinfo() <https://www.php.net/pathinfo>`_ function instead of string manipulations.

`pathinfo() <https://www.php.net/pathinfo>`_ is more efficient and readable and string functions.
When the path contains UTF-8 characters, `pathinfo() <https://www.php.net/pathinfo>`_ may strip them. There, string functions are necessary.

.. code-block:: php
   
   <?php
   
   $filename = '/path/to/file.php';
   
   // With pathinfo();
   $details = pathinfo($filename);
   print $details['extension'];  // also capture php
   
   // With string functions (other solutions possible)
   $ext = substr($filename, - strpos(strreverse($filename), '.')); // Capture php
   
   ?>
Connex PHP features
-------------------

  + `path <https://php-dictionary.readthedocs.io/en/latest/dictionary/path.ini.html>`_
  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Suggestions
___________

* Use pathinfo() and its second argument




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UsePathinfo                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-suitecrm-php-usepathinfo`                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


