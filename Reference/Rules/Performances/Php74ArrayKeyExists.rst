.. _performances-php74arraykeyexists:

.. _always-use-function-with-array\_key\_exists():

Always Use Function With array_key_exists()
+++++++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Always Use Function With array_key_exists(): array_key_exists() has been granted a special virtual machine opcode, and is much faster.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Always Use Function With array_key_exists()
	:twitter:description: Always Use Function With array_key_exists(): array_key_exists() has been granted a special virtual machine opcode, and is much faster
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Always Use Function With array_key_exists()
	:og:type: article
	:og:description: array_key_exists() has been granted a special virtual machine opcode, and is much faster
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Always Use Function With array_key_exists().html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/Php74ArrayKeyExists.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Performances\/Php74ArrayKeyExists.html","name":"Always Use Function With array_key_exists()","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"array_key_exists() has been granted a special virtual machine opcode, and is much faster","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Always Use Function With array_key_exists().html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`array_key_exists() <https://www.php.net/array_key_exists>`_ has been granted a special virtual machine opcode, and is much faster. This applies to PHP 7.4 and more recent. 

It requires that `array_key_exists() <https://www.php.net/array_key_exists>`_ is statically resolved, either with an initial ``\``, or a ``use function`` expression. This doesn't affect the global namespace.
This analysis is related to Php/ShouldUseFunction, and is a special case, that only concerns `array_key_exists() <https://www.php.net/array_key_exists>`_.

.. code-block:: php
   
   <?php
   
   namespace my/name/space;
   
   // do not forget the 'function' keyword, or it will apply to classes.
   use function array_key_exists as foo; // the alias is not necessary, and may be omitted.
   
   // array_key_exists is aliased to foo : 
   $c = foo($a, $b);
   
   // This call requires a fallback to global, and will be slow.
   $c = array_key_exists($a, $b);
   
   ?>

See also `Add array_key_exists to the list of specially compiled functions <https://bugs.php.net/bug.php?id=76148>`_.

Connex PHP features
-------------------

  + `vm <https://php-dictionary.readthedocs.io/en/latest/dictionary/vm.ini.html>`_
  + `opcode <https://php-dictionary.readthedocs.io/en/latest/dictionary/opcode.ini.html>`_


Suggestions
___________

* Use the `use` command for arrray_key_exists(), at the beginning of the script
* Use an initial \ before array_key_exists()
* Remove the namespace




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Short name   | Performances/Php74ArrayKeyExists                                                                                         |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Performances <ruleset-Performances>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.8.4                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.4 and more recent                                                                                             |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                    |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                          |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_  |
+--------------+--------------------------------------------------------------------------------------------------------------------------+


