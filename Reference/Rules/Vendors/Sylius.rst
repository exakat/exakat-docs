.. _vendors-sylius:

.. _sylius-usage:

Sylius usage
++++++++++++

  This analysis reports usage of the Sylius framework.

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


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Sylius                                                                                                          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`                                                              |
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
| Features     | framework                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


