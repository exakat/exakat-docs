.. _structures-mcryptcreateivwithoutoption:


.. _mcrypt\_create\_iv()-with-default-values:

mcrypt_create_iv() With Default Values
++++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		mcrypt_create_iv() With Default Values: Avoid using `mcrypt_create_iv()` default values.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: mcrypt_create_iv() With Default Values
	:twitter:description: mcrypt_create_iv() With Default Values: Avoid using `mcrypt_create_iv()` default values
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: mcrypt_create_iv() With Default Values
	:og:type: article
	:og:description: Avoid using `mcrypt_create_iv()` default values
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/mcrypt_create_iv() With Default Values.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/McryptcreateivWithoutOption.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/McryptcreateivWithoutOption.html","name":"mcrypt_create_iv() With Default Values","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using `mcrypt_create_iv()` default values","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/mcrypt_create_iv() With Default Values.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using `mcrypt_create_iv()` default values.

``mcrypt_create_iv()`` used to have ``MCRYPT_DEV_RANDOM`` as default values, and in PHP 5.6, it now uses ``MCRYPT_DEV_URANDOM``.

If the code doesn't have a second argument, it relies on the default value. It is recommended to set explicitly the value, so has to avoid problems while migrating.

.. code-block:: php
   
   <?php
       $size = mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB);
       // mcrypt_create_iv is missing the second argument
       $iv = mcrypt_create_iv($size);
   
   // Identical to the line below
   //    $iv = mcrypt_create_iv($size, MCRYPT_DEV_RANDOM);
   
   ?>

See also `mcrypt_create_iv() <https://www.php.net/manual/en/function.mcrypt-create-iv.php>`_.

Connex PHP features
-------------------

  + `mcrypt Extension <https://php-dictionary.readthedocs.io/en/latest/dictionary/mcrypt.ini.html>`_


Suggestions
___________

* Avoid using `mcrypt_create_iv()` default values.




Specs
_____

+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/McryptcreateivWithoutOption                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`CompatibilityPHP70 <ruleset-CompatibilityPHP70>` |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and older                                                                                                               |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                     |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                 |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_              |
+--------------+--------------------------------------------------------------------------------------------------------------------------------------+


