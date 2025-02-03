.. _structures-jsonwithoption:


.. _use-json\_decode()-options:

Use json_decode() Options
+++++++++++++++++++++++++


.. meta::

	:description:

		Use json_decode() Options: json_decode() returns objects by default, unless the second argument is set to ``TRUE`` or ``JSON_OBJECT_AS_ARRAY``.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use json_decode() Options

	:twitter:description: Use json_decode() Options: json_decode() returns objects by default, unless the second argument is set to ``TRUE`` or ``JSON_OBJECT_AS_ARRAY``

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use json_decode() Options

	:og:type: article

	:og:description: json_decode() returns objects by default, unless the second argument is set to ``TRUE`` or ``JSON_OBJECT_AS_ARRAY``

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use json_decode() Options.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/JsonWithOption.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/JsonWithOption.html","name":"Use json_decode() Options","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"json_decode() returns objects by default, unless the second argument is set to ``TRUE`` or ``JSON_OBJECT_AS_ARRAY``","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use json_decode() Options.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`json_decode() <https://www.php.net/json_decode>`_ returns objects by default, unless the second argument is set to ``TRUE`` or ``JSON_OBJECT_AS_ARRAY``. Then, it returns arrays.

Avoid casting the returned value from `json_decode() <https://www.php.net/json_decode>`_, and use the second argument to directly set the correct type.
Note that all objects will be turned into arrays, recursively. If you're expecting an array of objects, don't use the ``JSON_OBJECT_AS_ARRAY`` constant, and change your JSON code.

Note that ``JSON_OBJECT_AS_ARRAY`` is the only constant : there is no defined constant to explicitly ask for an object as returned value.

.. code-block:: php
   
   <?php
   
   $json = '{"a":"b"}';
   
   // Good syntax
   $array = json_decode($json, JSON_OBJECT_AS_ARRAY);
   
   // GoToo much work
   $array = (array) json_decode($json);
   
   ?>

See also `json_decode <https://www.php.net/json_decode>`_.

Connex PHP features
-------------------

  + `json <https://php-dictionary.readthedocs.io/en/latest/dictionary/json.ini.html>`_


Suggestions
___________

* Use the correct second argument of json_decode() : ``JSON_OBJECT_AS_ARRAY``




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/JsonWithOption                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.4.3                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


