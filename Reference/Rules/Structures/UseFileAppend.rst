.. _structures-usefileappend:


.. _use-file-append:

Use File Append
+++++++++++++++


.. meta::

	:description:

		Use File Append: When appending data to a file, one may also use the file_put_contents() function with the ``FILE_APPEND`` option.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Use File Append

	:twitter:description: Use File Append: When appending data to a file, one may also use the file_put_contents() function with the ``FILE_APPEND`` option

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Use File Append

	:og:type: article

	:og:description: When appending data to a file, one may also use the file_put_contents() function with the ``FILE_APPEND`` option

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use File Append.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseFileAppend.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/UseFileAppend.html","name":"Use File Append","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"When appending data to a file, one may also use the file_put_contents() function with the ``FILE_APPEND`` option","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Use File Append.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When appending data to a file, one may also use the `file_put_contents() <https://www.php.net/file_put_contents>`_ function with the ``FILE_APPEND`` option. 

Using `file_put_contents() <https://www.php.net/file_put_contents>`_ also keeps the file open as little as possible, unlike keeping the resource open in PHP, between usages.

.. code-block:: php
   
   <?php
   
   // appends the text to the end of the end of the file
   file_put_contents($file, $text, FILE_APPEND);
   
   // appends the text to the end of the end of the file
   $fp = fopen($file, 'a');
   fwrite($fp, $text);
   
   ?>
Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Suggestions
___________

* Use file_put_contents()




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/UseFileAppend                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.3.5                                                                                                                   |
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


