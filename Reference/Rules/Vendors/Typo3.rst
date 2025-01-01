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
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Typo3.html
	:og:locale: en
This rule reports usage of the Typo 3 CMS API in the code. 

TYPO3 is a free enterprise-class CMS based on PHP. It combines open source code with reliability and true scalability. 

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

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


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


