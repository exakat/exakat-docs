.. _extensions-extshmop:


.. _ext-shmop:

ext/shmop
+++++++++


.. meta::

	:description:

		ext/shmop: Extension ext/shmop.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/shmop

	:twitter:description: ext/shmop: Extension ext/shmop

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/shmop

	:og:type: article

	:og:description: Extension ext/shmop

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/shmop.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extshmop.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extshmop.html","name":"ext\/shmop","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ext\/shmop","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/shmop.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ext/`shmop <https://www.php.net/shmop>`_.

`Shmop <https://www.php.net/shmop>`_ is an easy to use set of functions that allows PHP to read, write, create and delete Unix shared memory segments.

.. code-block:: php
   
   <?php
   // Create a temporary file and return its path
   $tmp = tempnam('/tmp', 'PHP');
   
   // Get the file token key
   $key = ftok($tmp, 'a');
   
   // Attach the SHM resource, notice the cast afterwards
   $id = shm_attach($key);
   
   if ($id === false) {
       die('Unable to create the shared memory segment');
   }
   
   // Cast to integer, since prior to PHP 5.3.0 the resource id 
   // is returned which can be exposed when casting a resource
   // to an integer
   $id = (integer) $id;
   ?>

See also `Semaphore, Shared Memory and IPC <https://www.php.net/manual/en/book.sem.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extshmop                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


