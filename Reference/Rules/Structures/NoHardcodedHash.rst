.. _structures-nohardcodedhash:


.. _no-hardcoded-hash:

No Hardcoded Hash
+++++++++++++++++


.. meta::

	:description:

		No Hardcoded Hash: Hash should never be hardcoded.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No Hardcoded Hash

	:twitter:description: No Hardcoded Hash: Hash should never be hardcoded

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No Hardcoded Hash

	:og:type: article

	:og:description: Hash should never be hardcoded

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Hardcoded Hash.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoHardcodedHash.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoHardcodedHash.html","name":"No Hardcoded Hash","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Hash should never be hardcoded","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Hardcoded Hash.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Hash should never be hardcoded. 

Hashes may be MD5, SHA1, SHA512, Bcrypt or any other. Such values must be easily changed, for security reasons, and the source code is not the safest place to hide it.

.. code-block:: php
   
   <?php
   
       // Those strings may be sha512 hashes. 
       // it is recomemdned to check if they are static or should be put into configuration
       $init512 = array( // initial values for SHA512
           '6a09e667f3bcc908', 'bb67ae8584caa73b', '3c6ef372fe94f82b', 'a54ff53a5f1d36f1', 
       );
   
       // strings which are obvious conversion are ignored 
       $decimal = intval('87878877', 12);
   ?>

See also `Salted Password Hashing - Doing it Right <https://crackstation.net/hashing-security.htm>`_ and `Hash-Buster <https://github.com/s0md3v/Hash-Buster>`_.

Connex PHP features
-------------------

  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Put any hardcoded hash in a configuration file, a database or a environment variable. An external source.




Specs
_____

+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoHardcodedHash                                                                                                                         |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>` |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                              |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Critical                                                                                                                                           |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                      |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                          |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-shopware-structures-nohardcodedhash`, :ref:`case-sugarcrm-structures-nohardcodedhash`                                                   |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                            |
+--------------+----------------------------------------------------------------------------------------------------------------------------------------------------+


