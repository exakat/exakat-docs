.. _structures-directlyusefile:

.. _directly-use-file:

Directly Use File
+++++++++++++++++

.. meta::
	:description:
		Directly Use File: Some PHP functions have a close cousin that work directly on files.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Directly Use File
	:twitter:description: Directly Use File: Some PHP functions have a close cousin that work directly on files
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Directly Use File
	:og:type: article
	:og:description: Some PHP functions have a close cousin that work directly on files
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Directly Use File.html
	:og:locale: en
Some PHP functions have a close cousin that work directly on files. This is faster and less code to write.

* `md5() <https://www.php.net/md5>`_ => `md5_file() <https://www.php.net/md5_file>`_
* `highlight_string() <https://www.php.net/highlight_string>`_ => `highlight_file() <https://www.php.net/highlight_file>`_, `show_source() <https://www.php.net/show_source>`_
* parsekit_compile_string() => parsekit_compile_file()
* `parse_ini_string() <https://www.php.net/parse_ini_string>`_ => `parse_ini_file() <https://www.php.net/parse_ini_file>`_
* `sha1() <https://www.php.net/sha1>`_ => `sha1_file() <https://www.php.net/sha1_file>`_
* `simplexml_load_string() <https://www.php.net/simplexml_load_string>`_ => `simplexml_load_file() <https://www.php.net/simplexml_load_file>`_
* yaml_parse() => yaml_parse_file()
* `hash() <https://www.php.net/hash>`_ => `hash_file() <https://www.php.net/hash_file>`_
* `hash_hmac() <https://www.php.net/hash_hmac>`_ => hash_mac_file()
* `hash_update() <https://www.php.net/hash_update>`_ => `hash_update_file() <https://www.php.net/hash_update_file>`_
* recode() => recode_file()
* recode_string() => recode_file()

.. code-block:: php
   
   <?php
   
   // Good way
   $file_hash = hash_file('sha512', 'example.txt');
   
   // Slow way
   $file_hash = hash('sha512', file_get_contents('example.txt'));
   
   ?>

Suggestions
___________

* `hash_file <https://www.php.net/manual/en/function.hash-file.php>`_




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DirectlyUseFile                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


