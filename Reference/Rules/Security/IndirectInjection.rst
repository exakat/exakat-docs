.. _security-indirectinjection:


.. _indirect-injection:

Indirect Injection
++++++++++++++++++

.. meta::
	:description:
		Indirect Injection: This rule reports injections through indirect usage of $_GET, $_POST, $_REQUEST, $_COOKIE values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Indirect Injection
	:twitter:description: Indirect Injection: This rule reports injections through indirect usage of $_GET, $_POST, $_REQUEST, $_COOKIE values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Indirect Injection
	:og:type: article
	:og:description: This rule reports injections through indirect usage of $_GET, $_POST, $_REQUEST, $_COOKIE values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Indirect Injection.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/IndirectInjection.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/IndirectInjection.html","name":"Indirect Injection","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This rule reports injections through indirect usage of $_GET, $_POST, $_REQUEST, $_COOKIE values","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Indirect Injection.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports injections through indirect usage of `$_GET <https://www.php.net/manual/en/reserved.variables.get.php>`_, `$_POST <https://www.php.net/manual/en/reserved.variables.post.php>`_, `$_REQUEST <https://www.php.net/manual/en/reserved.variables.request.php>`_, $_COOKIE values. The injection is indirect, as the incoming data may be stored in different container before reaching the sensitive call. 

Sensitive parameters are identified with Security/`SensitiveParameter <https://www.php.net/sensitiveparameter>`_ rule.

.. code-block:: php
   
   <?php
   
   $a = $_GET['a'];
   echo $a;
   
   function foo($b) {
       echo $b;
   }
   foo($_POST['c']);  // $_POST is propagated to the foo function
   
   ?>
Connex PHP features
-------------------

  + `injection <https://php-dictionary.readthedocs.io/en/latest/dictionary/injection.ini.html>`_


Suggestions
___________

* Always validate incoming values before using them.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/IndirectInjection                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


