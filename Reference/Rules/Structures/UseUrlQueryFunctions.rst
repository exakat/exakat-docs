.. _structures-useurlqueryfunctions:

.. _should-use-url-query-functions:

Should Use Url Query Functions
++++++++++++++++++++++++++++++

.. meta::
	:description:
		Should Use Url Query Functions: PHP features several functions dedicated to processing URL's query string.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Url Query Functions
	:twitter:description: Should Use Url Query Functions: PHP features several functions dedicated to processing URL's query string
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Url Query Functions
	:og:type: article
	:og:description: PHP features several functions dedicated to processing URL's query string
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Should Use Url Query Functions.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseUrlQueryFunctions.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseUrlQueryFunctions.html","name":"Should Use Url Query Functions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP features several functions dedicated to processing URL's query string","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Should Use Url Query Functions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>PHP features several functions dedicated to processing URL's query string. 

+ `parse_str() <https://www.php.net/parse_str>`_
+ `parse_url() <https://www.php.net/parse_url>`_
+ `http_build_query() <https://www.php.net/http_build_query>`_

Those functions include extra checks : for example, `http_build_query() <https://www.php.net/http_build_query>`_ adds `urlencode() <https://www.php.net/urlencode>`_ call on the values, and allow for choosing the separator and the Query string format.

.. code-block:: php
   
   <?php
   $data = array(
       'foo' => 'bar',
       'baz' => 'boom',
       'cow' => 'milk',
       'php' => 'hypertext processor'
   );
   
   // safe and efficient way to build a query string
   echo http_build_query($data, '', '&') . PHP_EOL;
   
   // slow way to produce a query string
   foreach($data as $name => &$value) {
       $value = $name.'='.$value;
   }
   echo implode('&', $data) . PHP_EOL;
   
   ?>
Connex PHP features
-------------------

  + `url <https://php-dictionary.readthedocs.io/en/latest/dictionary/url.ini.html>`_


Suggestions
___________

* Use the URL query functions from PHP




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseUrlQueryFunctions                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.7                                                                                                                   |
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


