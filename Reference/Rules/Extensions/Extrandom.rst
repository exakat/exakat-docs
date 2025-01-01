.. _extensions-extrandom:

.. _random-extension:

Random extension
++++++++++++++++

.. meta::
	:description:
		Random extension: The random extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Random extension
	:twitter:description: Random extension: The random extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Random extension
	:og:type: article
	:og:description: The random extension
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extrandom.html
	:og:locale: en
The random extension. It improves the random generators from the older PHP version, and provides a OOP interface.

.. code-block:: php
   
   <?php
   
   $rng = $is_production
       ? new Random\Engine\Secure()
       : new Random\Engine\PCG64(1234);
    
   $randomizer = new Random\Randomizer($rng);
   $randomizer->shuffleString('foobar');
   
   ?>

See also `PHP RFC: Random Extension 5.x <https://wiki.php.net/rfc/rng_extension>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extrandom                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.4.7                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 8.2 and more recent                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


