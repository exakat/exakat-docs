.. _report-phpcity:

Phpcity
+++++++

Phpcity
_______

.. meta::
	:description:
		Phpcity: The Phpcity report represents your code as a city. .
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Phpcity
	:twitter:description: Phpcity: The Phpcity report represents your code as a city. 
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Phpcity
	:og:type: article
	:og:description: The Phpcity report represents your code as a city. 
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Phpcity report represents your code as a city. 

Phpcity is a code visualisation tool : it displays the source code as a city, with districts and buildings. There are be high sky crappers, signaling large classes, entire districts of small blocks, large venues and isolated parks. Some imagination is welcome too. 

The original idea is Richard Wettel's `Code city <https://wettel.github.io/codecity.html>`_, which has been adapted to many languages, including PHP. The PHP version is based on the open source `PHPcity project <https://github.com/adrianhuna/PHPCity>`_, which is itself build with `JScity <https://github.com/ASERG-UFMG/JSCity/wiki/JSCITY>`_. 

To use this tool, run an exakat audit, then generate the 'PHPcity' report : `php exakat.phar report -p mycode -format PHPcity -v`

This generates the `exakat.phpcity.json` file, in the `projects/mycode/` folder. 

You may test your own report online, at `Adrian Huna <https://github.com/adrianhuna>`_'s website, by `uploading the results <https://adrianhuna.github.io/PHPCity/>`_ and seeing it live immediately. 

Or, you can install the `PHPcity <https://github.com/adrianhuna/PHPCity>`_ application, and load it locally. 

.. image:: ../images/report.phpcity.png
    :alt: Example of a Phpcity report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Phpcity                                                          |
+--------------+------------------------------------------------------------------+
| Rulesets     | Phpcity doesn't depend on rulesets.                              |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | JSON                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.phpcity.json'.                 |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


