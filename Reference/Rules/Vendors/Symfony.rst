.. _vendors-symfony:

.. _symfony-usage:

Symfony usage
+++++++++++++

.. meta::
	:description:
		Symfony usage: This analysis reports usage of the Symfony framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Symfony usage
	:twitter:description: Symfony usage: This analysis reports usage of the Symfony framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Symfony usage
	:og:type: article
	:og:description: This analysis reports usage of the Symfony framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Symfony usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Symfony.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Symfony.html","name":"Symfony usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports usage of the Symfony framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Symfony usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This analysis reports usage of the Symfony framework.

.. code-block:: php
   
   <?php
   
   // src/AppBundle/Controller/LuckyController.php
   namespace AppBundle\Controller;
   
   use Sensio\Bundle\FrameworkExtraBundle\Configuration\Route;
   use Symfony\Component\HttpFoundation\Response;
   
   class LuckyController
   {
       /**
        * @Route("/lucky/number")
        */
       public function numberAction()
       {
           $number = mt_rand(0, 100);
   
           return new Response(
               '<html><body>Lucky number: '.$number.'</body></html>'
           );
       }
   }
   
   ?>

See also `Symfony <http://www.symfony.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Symfony                                                                                                                                                                         |
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


