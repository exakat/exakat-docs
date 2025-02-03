.. _vendors-sylius:

.. _sylius-usage:

Sylius usage
++++++++++++

.. meta::
	:description:
		Sylius usage: This analysis reports usage of the Sylius framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Sylius usage
	:twitter:description: Sylius usage: This analysis reports usage of the Sylius framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Sylius usage
	:og:type: article
	:og:description: This analysis reports usage of the Sylius framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Sylius usage.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Sylius.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Vendors\/Sylius.html","name":"Sylius usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This analysis reports usage of the Sylius framework","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Sylius usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>This analysis reports usage of the Sylius framework.

Sylius is an Open Source Headless eCommerce Platform for mid-market and enterprise brands that need custom solutions.

.. code-block:: php
   
   <?php
   
   declare(strict_types=1);
   
   namespace App\Controller;
   
   use Sylius\Bundle\ResourceBundle\Controller\ResourceController;
   use Sylius\Component\Resource\ResourceActions;
   use Symfony\Component\HttpFoundation\Request;
   use Symfony\Component\HttpFoundation\Response;
   
   class ProductController extends ResourceController
   {
       public function showAction(Request $request): Response
       {
           $configuration = $this->requestConfigurationFactory->create($this->metadata, $request);
   
           $this->isGrantedOr403($configuration, ResourceActions::SHOW);
           $product = $this->findOr404($configuration);
   
           // some custom provider service to retrieve recommended products
           $recommendationService = $this->get('app.provider.product');
   
           $recommendedProducts = $recommendationService->getRecommendedProducts($product);
   
           $this->eventDispatcher->dispatch(ResourceActions::SHOW, $configuration, $product);
   
           if ($configuration->isHtmlRequest()) {
               return $this->render($configuration->getTemplate(ResourceActions::SHOW . '.html'), [
                   'configuration' => $configuration,
                   'metadata' => $this->metadata,
                   'resource' => $product,
                   'recommendedProducts' => $recommendedProducts,
                   $this->metadata->getName() => $product,
               ]);
           }
   
           return $this->createRestView($configuration, $product);
       }
   }
   
   ?>

See also `sylius <https://sylius.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Sylius                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


