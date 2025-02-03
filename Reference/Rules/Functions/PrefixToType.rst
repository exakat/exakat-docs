.. _functions-prefixtotype:


.. _prefix-and-suffixes-with-type:

Prefix And Suffixes With Type
+++++++++++++++++++++++++++++


.. meta::

	:description:

		Prefix And Suffixes With Type: This analysis checks the relationship between methods prefixes and suffixes, with their corresponding return type.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Prefix And Suffixes With Type

	:twitter:description: Prefix And Suffixes With Type: This analysis checks the relationship between methods prefixes and suffixes, with their corresponding return type

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Prefix And Suffixes With Type

	:og:type: article

	:og:description: This analysis checks the relationship between methods prefixes and suffixes, with their corresponding return type

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Prefix And Suffixes With Type.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/PrefixToType.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/PrefixToType.html","name":"Prefix And Suffixes With Type","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 24 Jan 2025 10:21:35 +0000","dateModified":"Fri, 24 Jan 2025 10:21:35 +0000","description":"This analysis checks the relationship between methods prefixes and suffixes, with their corresponding return type","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Prefix And Suffixes With Type.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This analysis checks the relationship between methods prefixes and suffixes, with their corresponding return type.

For example, a method with the signature ``function isACustomer() {}`` should return a boolean. That boolean can then be read when calling the method : ``if ($user->isACustomer()) {}``.

There are multiple such conventions that may be applied. For example, ``has*`` should return a boolean, ``set*`` should return nothing (aka ``void``), and ``get*`` shall return any kind of type. 
There are 2 parameters for this analysis. It is recommended to customize them to get an better results, related to the naming conventions used in the code.

``prefixedType`` is used for prefix in method names, which is the beginning of the name. ``suffixedType`` is used for suffixes : the ending part of the name. Matching is case insensitive.

The prefix is configured as the index of the map, while the related type is configured as the value of the map.

``prefixToType['is'] = 'bool';`` will be use as ``is*`` shall use the ``bool`` type.

Multiple types may be used at the same time. PHP supports multiple types since PHP 8.0, and Exakat will support them with any PHP version. Specify multiple types by separating them with comma. Any type not found in this list will be reported, including ``null``.

PHP scalar types are available : ``string``, ``int``, ``void``, etc. Explicit types, based on classes or interfaces, must use the fully qualified name, not the short name. ``suffixToType['uuid'] = '\Uuid';`` will be use as ``*uuid`` shall use the ``\Uuid`` type.

When multiple rules applies, only one is reported.

.. code-block:: php
   
   <?php
   
   class x  {
       // Easy to read convention
       function isAUser() : bool {}
   
       // shall return a boolean
       function isACustomer() {}
   
       // shall return a string, based on suffix 'name => string'
       function getName() {}
   
       // shall return a string, based on suffix 'name => string'
       function getUsername() {}
   
       // shall return \Uuid, based on prefix 'uuid => \Uuid'
       function getUuid() {}
   
       // shall return anything, based on no prefix nor suffix
       function getBirthday() {}
   
   }
   
   ?>

+--------------+-----------------------------------------+----------+------------------------------------------------+
| Name         | Default                                 | Type     | Description                                    |
+--------------+-----------------------------------------+----------+------------------------------------------------+
| prefixedType | prefixedType['is'] = 'bool';            | ini_hash | List of prefixes and their expected returntype |
|              | prefixedType['has'] = 'bool';           |          |                                                |
|              | prefixedType['set'] = 'void';           |          |                                                |
|              | prefixedType['list'] = 'array';         |          |                                                |
+--------------+-----------------------------------------+----------+------------------------------------------------+
| suffixedType | prefixedType['list'] = 'bool';          | ini_hash | List of suffixes and their expected returntype |
|              | prefixedType['int'] = 'int';            |          |                                                |
|              | prefixedType['string'] = 'string';      |          |                                                |
|              | prefixedType['name'] = 'string';        |          |                                                |
|              | prefixedType['description'] = 'string'; |          |                                                |
|              | prefixedType['id'] = 'int';             |          |                                                |
|              | prefixedType['uuid'] = '\Uuid';         |          |                                                |
+--------------+-----------------------------------------+----------+------------------------------------------------+



Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/PrefixToType                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Semantics <ruleset-Semantics>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.1.1                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


