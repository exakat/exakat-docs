.. _vendors-drupal:

.. _drupal-usage:

Drupal Usage
++++++++++++

.. meta\:\:
	:description:
		Drupal Usage: This analysis reports usage of the Drupal CMS.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Drupal Usage
	:twitter:description: Drupal Usage: This analysis reports usage of the Drupal CMS
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Drupal Usage
	:og:type: article
	:og:description: This analysis reports usage of the Drupal CMS
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Drupal.html
	:og:locale: en
  This analysis reports usage of the Drupal CMS. The report is based on the usage of Drupal namespace.

.. code-block:: php
   
   <?php
   
   namespace Drupal\example\Controller;
   
   use Drupal\Core\Controller\ControllerBase;
   
   /**
    * An example controller.
    */
   class ExampleController extends ControllerBase {
   
     /**
      * {@inheritdoc}
      */
     public function content() {
       $build = array(
         '#type' => 'markup',
         '#markup' => t('Hello World!'),
       );
       return $build;
     }
   
   }
   
   ?>

See also `Drupal <http://www.drupal.org/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Drupal                                                                                                                                                                          |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.0.3                                                                                                                                                                                   |
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


