.. _report-json:

Json
++++

Json
____

.. meta::
	:description:
		Json: The JSON report exports in JSON format..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Json
	:twitter:description: Json: The JSON report exports in JSON format.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Json
	:og:type: article
	:og:description: The JSON report exports in JSON format.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The JSON report exports in JSON format.

Simple Json format. It is a structured array with all results, described as object.

::

    Filename => [
                    errors   => count,
                    warning  => count,
                    fixable  => count,
                    filename => string,
                    message  => [
                        line => [
                            type,
                            source,
                            severity,
                            fixable,
                            message
                        ]
                    ]
                ]




::

    {  
       "\/src\/Path\/To\/File.php":{  
          "errors":0,
          "warnings":105,
          "fixable":0,
          "filename":"\/src\/Path\/To\/File.php",
          "messages":{  
             "55":[  
                [  
                   {  
                      "type":"warning",
                      "source":"Php/EllipsisUsage",
                      "severity":"Major",
                      "fixable":"fixable",
                      "message":"... Usage"
                   }
                ]
             ],
             }
        }
    }

.. image:: ../images/report.json.png
    :alt: Example of a Json report (1)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Json                                                             |
+--------------+------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.            |
|              |                                                                  |
|              |                                                                  |
+--------------+------------------------------------------------------------------+
| Type         | Json                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.json'.                         |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


