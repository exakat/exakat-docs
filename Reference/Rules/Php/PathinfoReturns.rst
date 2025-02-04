.. _php-pathinforeturns:


.. _pathinfo()-returns-may-vary:

Pathinfo() Returns May Vary
+++++++++++++++++++++++++++

.. meta::
	:description:
		Pathinfo() Returns May Vary: pathinfo() function returns an array whose content may vary.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Pathinfo() Returns May Vary
	:twitter:description: Pathinfo() Returns May Vary: pathinfo() function returns an array whose content may vary
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Pathinfo() Returns May Vary
	:og:type: article
	:og:description: pathinfo() function returns an array whose content may vary
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Pathinfo() Returns May Vary.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PathinfoReturns.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/PathinfoReturns.html","name":"Pathinfo() Returns May Vary","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"pathinfo() function returns an array whose content may vary","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Pathinfo() Returns May Vary.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`pathinfo() <https://www.php.net/pathinfo>`_ function returns an array whose content may vary. It is recommended to collect the values after check, rather than directly.
The same applies to `parse_url() <https://www.php.net/parse_url>`_, which returns an array with various index.

.. code-block:: php
   
   <?php
   
   $file = '/a/b/.c';
   //$extension may be missing, leading to empty $filename and filename in $extension
   list( $dirname, $basename, $extension, $filename ) = array_values( pathinfo($file) );
   
   //Use PHP 7.1 list() syntax to assign correctly the values, and skip array_values()
   //This emits a warning in case of missing index
   ['dirname'   => $dirname, 
    'basename'  => $basename, 
    'extension' => $extension, 
    'filename'  => $filename ] = pathinfo($file);
    
   //This works without warning
   $details = pathinfo($file);
   $dirname   = $details['dirname'] ?? getpwd();
   $basename  = $details['basename'] ?? '';
   $extension = $details['extension'] ?? '';
   $filename  = $details['filename'] ?? '';
   
   ?>
Connex PHP features
-------------------

  + `Path <https://php-dictionary.readthedocs.io/en/latest/dictionary/path.ini.html>`_


Suggestions
___________

* Add a check on the return value of pathinfo() before using it.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/PathinfoReturns                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.11                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-nextcloud-php-pathinforeturns`                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


