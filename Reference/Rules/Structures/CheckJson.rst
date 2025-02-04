.. _structures-checkjson:


.. _check-json:

Check JSON
++++++++++

.. meta::
	:description:
		Check JSON: Check errors whenever JSON is encoded or decoded.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Check JSON
	:twitter:description: Check JSON: Check errors whenever JSON is encoded or decoded
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Check JSON
	:og:type: article
	:og:description: Check errors whenever JSON is encoded or decoded
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Check JSON.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckJson.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/CheckJson.html","name":"Check JSON","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Check errors whenever JSON is encoded or decoded","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Check JSON.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Check errors whenever JSON is encoded or decoded. 

In particular, ``NULL`` is a valid decoded JSON response. If you want to avoid mistaking `NULL <https://www.php.net/manual/en/language.types.`null <https://www.php.net/null>`_.php>`_ for an `error <https://www.php.net/error>`_, it is recommended to call ``json_last_error``.

.. code-block:: php
   
   <?php
   
   $encoded = json_encode($incoming);
   // Unless JSON must contains some non-null data, this mistakes NULL and error
   if(json_last_error() != JSON_ERROR_NONE) {
       die('Error when encoding JSON');
   }
   
   $decoded = json_decode($incoming);
   // Unless JSON must contains some non-null data, this mistakes NULL and error
   if($decoded === null) {
       die('ERROR');
   }
   
   ?>

See also `Option to make json_encode and json_decode throw exceptions on errors <https://ayesh.me/Upgrade-PHP-7.3#json-exceptions>`_ and `json_last_error <https://www.php.net/json_last_error>`_.

Connex PHP features
-------------------

  + `JavaScript Object Notation (JSON) <https://php-dictionary.readthedocs.io/en/latest/dictionary/json.ini.html>`_


Suggestions
___________

* Always check after JSON operation : encoding or decoding.
* Add a call to json_last_error()
* Configure operations to throw an exception upon error (``JSON_THROW_ON_ERROR``), and catch it.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/CheckJson                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-woocommerce-structures-checkjson`                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


