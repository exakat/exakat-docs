.. _vendors-codeigniter:

.. _codeigniter-usage:

Codeigniter usage
+++++++++++++++++

.. meta::
	:description:
		Codeigniter usage: This analysis reports usage of the Codeigniter 4 framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Codeigniter usage
	:twitter:description: Codeigniter usage: This analysis reports usage of the Codeigniter 4 framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Codeigniter usage
	:og:type: article
	:og:description: This analysis reports usage of the Codeigniter 4 framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Codeigniter usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Codeigniter.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Codeigniter.html","name":"Codeigniter usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports usage of the Codeigniter 4 framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Codeigniter usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This analysis reports usage of the Codeigniter 4 framework.

Note : Code igniter 3 and older are not reported.

.. code-block:: php
   
   <?php
   
   // A code igniter controller
   class Blog extends \App\Controllers\Home {
   
           public function index()
           {
                   echo 'Hello World!';
           }
   }
   
   ?>

See also `Codeigniter <https://codeigniter.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Codeigniter                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.8                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


