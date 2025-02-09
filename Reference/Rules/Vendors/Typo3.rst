.. _vendors-typo3:


.. _typo-3-usage:

Typo 3 usage
++++++++++++

.. meta::
	:description:
		Typo 3 usage: This rule reports usage of the Typo 3 CMS API in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Typo 3 usage
	:twitter:description: Typo 3 usage: This rule reports usage of the Typo 3 CMS API in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Typo 3 usage
	:og:type: article
	:og:description: This rule reports usage of the Typo 3 CMS API in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Typo 3 usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Typo3.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Typo3.html","name":"Typo 3 usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"This rule reports usage of the Typo 3 CMS API in the code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Typo 3 usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This rule reports usage of the Typo 3 CMS API in the code. 

TYPO3 is a free enterprise-class CMS based on PHP. It combines open source code with reliability and `true <https://www.php.net/true>`_ scalability. 

.. code-block:: php
   
   <?php
   declare(strict_types=1);
   
   namespace MyVendor\SjrOffers\Controller;
   
   use TYPO3\CMS\Extbase\Mvc\Controller\ActionController;
   
   class OfferController extends ActionController
   {
      // action methods will be following here
   }
   ?>

See also `Typo3 <https://typo3.org/>`_.

Connex PHP features
-------------------

  + `Framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Typo3                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
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


