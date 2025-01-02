.. _report-marmelab:

Marmelab
++++++++

Marmelab
________

.. meta::
	:description:
		Marmelab: The Marmelab report format data to use with a GraphQL server..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Marmelab
	:twitter:description: Marmelab: The Marmelab report format data to use with a GraphQL server.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Marmelab
	:og:type: article
	:og:description: The Marmelab report format data to use with a GraphQL server.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The Marmelab report format data to use with a GraphQL server.

Marmelab is a report format to build GraphQL server with exakat's results. Export the results of the audit in this JSON file, then use the `json-graphql-server <https://github.com/marmelab/json-graphql-server>`_ to have a GraphQL server with all the results.

You may also learn more about GraphQL at `Introducing Json GraphQL Server <https://marmelab.com/blog/2017/07/12/json-graphql-server.html>`_.

::

    php exakat.phar report -p -format Marmelab -file marmelab
    cp projects/myproject/marmelab.json path/to/marmelab
    json-graphql-server db.json
    



Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Marmelab                                                         |
+--------------+------------------------------------------------------------------+
| Rulesets     | Analyze.                                                         |
+--------------+------------------------------------------------------------------+
| Type         | JSON                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'exakat.json'.                         |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


