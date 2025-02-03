.. _security-unserializesecondarg:

.. _unserialize-second-arg:

Unserialize Second Arg
++++++++++++++++++++++

.. meta::
	:description:
		Unserialize Second Arg: Since PHP 7, unserialize() function has a second argument that limits the classes that may be unserialized.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unserialize Second Arg
	:twitter:description: Unserialize Second Arg: Since PHP 7, unserialize() function has a second argument that limits the classes that may be unserialized
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unserialize Second Arg
	:og:type: article
	:og:description: Since PHP 7, unserialize() function has a second argument that limits the classes that may be unserialized
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Unserialize Second Arg.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/UnserializeSecondArg.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/UnserializeSecondArg.html","name":"Unserialize Second Arg","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Since PHP 7, unserialize() function has a second argument that limits the classes that may be unserialized","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Unserialize Second Arg.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Since PHP 7, `unserialize() <https://www.php.net/unserialize>`_ function has a second argument that limits the classes that may be unserialized. In case of a breach, this is limiting the classes accessible from `unserialize() <https://www.php.net/unserialize>`_. 

One way to exploit unserialize, is to make PHP unserialized the data to an available class, may be one that may be auto-loaded.

.. code-block:: php
   
   <?php
   
   // safe unserialization : only the expected class will be extracted
   $serialized = 'O:7:"dbClass":0:{}';
   $var = unserialize($serialized, ['dbClass']);
   $var->connect();
   
   // unsafe unserialization : $var may be of any type that was in the serialized string
   // although, here, this is working well.
   $serialized = 'O:7:"dbClass":0:{}';
   $var = unserialize($serialized);
   $var->connect();
   
   // unsafe unserialization : $var is not of the expected type.
   // and, here, this will lead to disaster.
   $serialized = 'O:10:"debugClass":0:{}';
   $var = unserialize($serialized);
   $var->connect();
   
   ?>

See also `unserialize() <https://www.php.net/unserialize>`_, `Securely Implementing (De)Serialization in PHP <https://paragonie.com/blog/2016/04/securely-implementing-de-serialization-in-php>`_ and `Remote code execution via PHP [Unserialize] <https://www.notsosecure.com/remote-code-execution-via-php-unserialize/>`_.

Connex PHP features
-------------------

  + `serialization <https://php-dictionary.readthedocs.io/en/latest/dictionary/serialization.ini.html>`_


Suggestions
___________

* Add a list of class as second argument of any call to unserialize(). This is valid for PHP 7.0 and later.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/UnserializeSecondArg                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-piwigo-security-unserializesecondarg`, :ref:`case-livezilla-security-unserializesecondarg`                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


