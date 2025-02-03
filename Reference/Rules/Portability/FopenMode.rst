.. _portability-fopenmode:


.. _fopen-binary-mode:

Fopen Binary Mode
+++++++++++++++++


.. meta::

	:description:

		Fopen Binary Mode: Use explicit ``b`` when opening files.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Fopen Binary Mode

	:twitter:description: Fopen Binary Mode: Use explicit ``b`` when opening files

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Fopen Binary Mode

	:og:type: article

	:og:description: Use explicit ``b`` when opening files

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Fopen Binary Mode.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/FopenMode.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Portability\/FopenMode.html","name":"Fopen Binary Mode","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Use explicit ``b`` when opening files","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Fopen Binary Mode.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Use explicit ``b`` when opening files.

`fopen() <https://www.php.net/fopen>`_ supports a ``b`` option in the second parameter, to make sure the read is binary. This is the recommended way when writing portable applications, between Linux and Windows.
Also, Windows PHP does support a ``t`` option, that translates automatically line endings to the right value. As this is Windows only, this should be avoided for portability reasons.

.. code-block:: php
   
   <?php
   
   // This opens file with binary reads on every OS
   $fp = fopen('path/to/file.doc', 'wb');
   
   // This may not open files with binary mode on Windows
   $fp = fopen('path/to/file.doc', 'w');
   
   ?>

See also `fopen <https://www.php.net/fopen>`_.

Connex PHP features
-------------------

  + `file <https://php-dictionary.readthedocs.io/en/latest/dictionary/file.ini.html>`_


Suggestions
___________

* Add the `b` option when opening files




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/FopenMode                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


