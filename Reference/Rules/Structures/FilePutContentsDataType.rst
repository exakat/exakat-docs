.. _structures-fileputcontentsdatatype:


.. _file\_put\_contents-using-array-argument:

File_Put_Contents Using Array Argument
++++++++++++++++++++++++++++++++++++++


.. meta::

	:description:

		File_Put_Contents Using Array Argument: file_put_contents() accepts a second argument as an array, and stores it in the file with an implicit implode.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: File_Put_Contents Using Array Argument

	:twitter:description: File_Put_Contents Using Array Argument: file_put_contents() accepts a second argument as an array, and stores it in the file with an implicit implode

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: File_Put_Contents Using Array Argument

	:og:type: article

	:og:description: file_put_contents() accepts a second argument as an array, and stores it in the file with an implicit implode

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/File_Put_Contents Using Array Argument.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FilePutContentsDataType.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/FilePutContentsDataType.html","name":"File_Put_Contents Using Array Argument","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"file_put_contents() accepts a second argument as an array, and stores it in the file with an implicit implode","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/File_Put_Contents Using Array Argument.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`file_put_contents() <https://www.php.net/file_put_contents>`_ accepts a second argument as an array, and stores it in the file with an implicit implode. This is a documented behavior, though it is rarely used.

.. code-block:: php
   
   <?php
   
   file_put_contents('/tmp/file.txt', [1, 2, 3, 4]);
   
   print file_get_contents('/tmp/file.txt'); 
   // displays 1234
   
   ?>

See also `file_put_contents() <https://www.php.net/file_put_contents>`_.

Connex PHP features
-------------------

  + `silent <https://php-dictionary.readthedocs.io/en/latest/dictionary/silent.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/FilePutContentsDataType                                                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.5                                                                                                                   |
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


