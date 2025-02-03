.. _structures-possibleinfiniteloop:

.. _possible-infinite-loop:

Possible Infinite Loop
++++++++++++++++++++++

.. meta::
	:description:
		Possible Infinite Loop: Loops on files that can't be open results in infinite loop.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Possible Infinite Loop
	:twitter:description: Possible Infinite Loop: Loops on files that can't be open results in infinite loop
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Possible Infinite Loop
	:og:type: article
	:og:description: Loops on files that can't be open results in infinite loop
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Possible Infinite Loop.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PossibleInfiniteLoop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/PossibleInfiniteLoop.html","name":"Possible Infinite Loop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Loops on files that can't be open results in infinite loop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Possible Infinite Loop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Loops on files that can't be open results in infinite loop.

`fgets() <https://www.php.net/fgets>`_, and functions like `fgetss() <https://www.php.net/fgetss>`_, `fgetcsv() <https://www.php.net/fgetcsv>`_, `fread() <https://www.php.net/fread>`_, return false when they finish reading, or can't access the file. 

In case the file is not accessible, comparing the `result <https://www.php.net/result>`_ of the reading to something that is falsy, leads to a permanent valid condition. The execution will only finish when the ``max_execution_time`` is reached. 
It is recommended to check the file resources when they are opened, and always use === or !== to compare readings. `feof() <https://www.php.net/feof>`_ is also a reliable function here.

.. code-block:: php
   
   <?php
   
   $file = fopen('/path/to/file.txt', 'r');
   // when fopen() fails, the next loops is infinite
   // fgets() will always return false, and while will always be true. 
   while($line = fgets($file) != 'a') {
       doSomething();
   }
   
   ?>
Connex PHP features
-------------------

  + `loop <https://php-dictionary.readthedocs.io/en/latest/dictionary/loop.ini.html>`_


Suggestions
___________

* Add a check before using the result of the method.
* Add a counter to break the loop after a limit of loops.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/PossibleInfiniteLoop                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.1.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


