.. _report-composer:

Composer
++++++++

Composer
________

.. meta::
	:description:
		Composer: The Composer report provide elements for the require attribute in the composer.json..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Composer
	:twitter:description: Composer: The Composer report provide elements for the require attribute in the composer.json.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Composer
	:og:type: article
	:og:description: The Composer report provide elements for the require attribute in the composer.json.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Composer report provide elements for the require attribute in the composer.json.

It helps documenting the composer.json, by providing more information, extracted from the code.

This report makes a copy then updates the composer.json, when available; otherwise, it creates a totally new composer.json. 

The report provides a calculated value for "php": "^7.3" and all the identified PHP extensions (such as "ext-exif", "ext-gd", "ext-finfo", etc). Core PHP extensions are omitted. 

It is recommended to review manually the results of the suggested composer.json before using it.



::

    Name,File,Line
    0,/features/bootstrap/FeatureContext.php,61
    10000,/features/bootstrap/FeatureContext.php,61
    777,/features/bootstrap/FeatureContext.php,63
    20,/features/bootstrap/FeatureContext.php,73
    0,/features/bootstrap/FeatureContext.php,334
    0,/features/bootstrap/FeatureContext.php,339
    0,/features/bootstrap/FeatureContext.php,344
    0,/features/bootstrap/FeatureContext.php,362
    0,/features/bootstrap/FeatureContext.php,366
    0,/features/bootstrap/FeatureContext.php,368
    0,/features/bootstrap/FeatureContext.php,372
    777,/features/bootstrap/FeatureContext.php,423
    777,/features/bootstrap/FeatureContext.php,431
    0,/src/Behat/Behat/Context/ContextClass/SimpleClassGenerator.php,68
    1,/src/Behat/Behat/Context/ContextClass/SimpleClassGenerator.php,69
    0,/src/Behat/Behat/Context/Environment/InitializedContextEnvironment.php,84
    0,/src/Behat/Behat/Context/Environment/InitializedContextEnvironment.php,150
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Composer                                                         |
+--------------+------------------------------------------------------------------+
| Rulesets     | Appinfo.                                                         |
+--------------+------------------------------------------------------------------+
| Type         | JSON                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'composer.json'.                       |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


