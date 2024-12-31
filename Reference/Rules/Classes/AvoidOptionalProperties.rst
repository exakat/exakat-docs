.. _classes-avoidoptionalproperties:

.. _avoid-optional-properties:

Avoid Optional Properties
+++++++++++++++++++++++++

.. meta\:\:
	:description:
		Avoid Optional Properties: Avoid optional properties, to prevent littering the code with existence checks.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Avoid Optional Properties
	:twitter:description: Avoid Optional Properties: Avoid optional properties, to prevent littering the code with existence checks
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Avoid Optional Properties
	:og:type: article
	:og:description: Avoid optional properties, to prevent littering the code with existence checks
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Classes/AvoidOptionalProperties.html
	:og:locale: en
  Avoid optional properties, to prevent littering the code with existence checks. 

When a property has to be checked once for existence, it is safer to check it each time. This leads to a decrease in readability and a lot of checks added to the code.

Either make sure the property is set with an actual object rather than with null, or use a null object. A null object offers the same interface than the expected object, but does nothing. It allows calling its methods, without running into a Fatal `error <https://www.php.net/error>`_, nor testing it.

.. code-block:: php
   
   <?php
   
   // Example is courtesy 'The Coding Machine' : it has been adapted from its original form. See link below.
   
   class MyMailer {
       private $logger;
   
       public function __construct(LoggerInterface $logger = null) {
           $this->logger = $logger;
       }
   
       private function sendMail(Mail $mail) {
           // Since $this->logger may be null, it must be tested anytime it is used.
           if ($this->logger) {
               $this->logger->info('Mail successfully sent.');
           }
       }
   }
   
   ?>

See also `Avoid optional services as much as possible <http://bestpractices.thecodingmachine.com/php/design_beautiful_classes_and_methods.html#avoid-optional-services-as-much-as-possible>`_, `The Null Object Pattern – Polymorphism in Domain Models <https://www.sitepoint.com/the-null-object-pattern-polymorphism-in-domain-models/>`_ and `Practical PHP Refactoring: Introduce Null Object <https://dzone.com/articles/practical-php-refactoring-26>`_.

Connex PHP features
-------------------

  + `property <https://php-dictionary.readthedocs.io/en/latest/dictionary/property.ini.html>`_
  + `null <https://php-dictionary.readthedocs.io/en/latest/dictionary/null.ini.html>`_


Suggestions
___________

* Use a null object to fill any missing value
* Make sure the property is set at constructor time




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Classes/AvoidOptionalProperties                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.0                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-classes-avoidoptionalproperties`, :ref:`case-dolibarr-classes-avoidoptionalproperties`             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


