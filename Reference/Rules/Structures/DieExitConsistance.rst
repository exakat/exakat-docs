.. _structures-dieexitconsistance:

.. _die-exit-consistence:

Die Exit Consistence
++++++++++++++++++++

.. meta::
	:description:
		Die Exit Consistence: Die and Exit have the same functional use.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Die Exit Consistence
	:twitter:description: Die Exit Consistence: Die and Exit have the same functional use
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Die Exit Consistence
	:og:type: article
	:og:description: Die and Exit have the same functional use
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Die Exit Consistence.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DieExitConsistance.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/DieExitConsistance.html","name":"Die Exit Consistence","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Die and Exit have the same functional use","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Die Exit Consistence.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`Die <https://www.php.net/die>`_ and `Exit <https://www.www.php.net/exit>`_ have the same functional use. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make them all the same. 

It happens that `die <https://www.php.net/die>`_ or `exit <https://www.www.php.net/exit>`_ are used depending on coding style and files. One file may be consistently using `exit <https://www.www.php.net/exit>`_, while the others are all using `exit <https://www.www.php.net/exit>`_. 

Using `die <https://www.php.net/die>`_ or `exit <https://www.www.php.net/exit>`_ is also the target of other analysis.

.. code-block:: php
   
   <?php
   
   // be consistent
   switch ($a) {
       case 1 : 
           exit;
       case 2 : 
           exit;
       case 3 : 
           exit;
       case 4 : 
           exit;
       case 5 : 
           exit;
       case 6 : 
           exit;
       case 7 : 
           exit;
       case 8 : 
           exit;
       case 9 : 
           exit;
       case 10 : 
           exit;
       default : 
           die();   // Be consistent, always use the same. 
   }
   
   ?>
Connex PHP features
-------------------

  + `die <https://php-dictionary.readthedocs.io/en/latest/dictionary/die.ini.html>`_


Suggestions
___________

* Adopt one of the two syntaxes




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/DieExitConsistance                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Preferences <ruleset-Preferences>`                                                      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.9                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


