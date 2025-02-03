.. _extensions-extv8js:

.. _ext-v8js:

ext/v8js
++++++++

.. meta::
	:description:
		ext/v8js: Extension v8js.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/v8js
	:twitter:description: ext/v8js: Extension v8js
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/v8js
	:og:type: article
	:og:description: Extension v8js
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/v8js.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extv8js.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extv8js.html","name":"ext\/v8js","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension v8js","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/v8js.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Extension v8js.

This extension embeds the `V8 Javascript `Engine <https://www.php.net/engine>`_ <https://bugs.chromium.org/p/v8/issues/list>`_ into PHP.

.. code-block:: php
   
   <?php
   
   $v8 = new V8Js();
   
   /* basic.js */
   $JS = <<< EOT
   len = print('Hello' + ' ' + 'World!' + '\n');
   len;
   EOT;
   
   try {
     var_dump($v8->executeString($JS, 'basic.js'));
   } catch (V8JsException $e) {
     var_dump($e);
   }
   
   ?>

See also `V8 Javascript Engine Integration <https://www.php.net/manual/en/book.v8js.php>`_, `V8 Javascript Engine for PHP <https://github.com/phpv8/v8js>`_ and `pecl v8js <https://pecl.php.net/package/v8js>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extv8js                                                                                                                                                                      |
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


