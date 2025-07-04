.. _report-typesuggestion:

TypeSuggestion
++++++++++++++

TypeSuggestion
______________

.. meta::
	:description:
		TypeSuggestion: The TypeSuggestion report provides suggestions to add typehints to methods and properties..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: TypeSuggestion
	:twitter:description: TypeSuggestion: The TypeSuggestion report provides suggestions to add typehints to methods and properties.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: TypeSuggestion
	:og:type: article
	:og:description: The TypeSuggestion report provides suggestions to add typehints to methods and properties.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

The TypeSuggestion report provides suggestions to add typehints to methods and properties.

The TypeSuggestion offers suggestions to add typehints to methods and properties. 

It provides its suggestion based on the way the code is implemented : by usage or by calling.

Type usage is the way a typed container is use later. For example, an argument that is used later with the array syntax ``$x['a']`` or as an object ``$x->b``will receive a suggestion for using array or object.

Type calling is the way the typed container is assigned. For example, a property may receive integer or boolean during assignations : they will receive such suggestions. 

Not all types can be guessed : for example, a property may simply hold a value, for later use, such as in a cache system. In such situation, no type is suggested.

``mixed`` is not used as suggestion : rather a list of possible types is offered, and it may be upgraded to ``mixed``. 

This report is ready for PHP 8.0 : the suggestions may be combined together, and multiples suggestions are possible. 


.. image:: ../images/report.typesuggestion.png
    :alt: Example of a TypeSuggestion report (0)

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | TypeSuggestion                                                   |
+--------------+------------------------------------------------------------------+
| Rulesets     | TypeChecks.                                                      |
+--------------+------------------------------------------------------------------+
| Type         | HTML                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'typehint.suggestion.html'.            |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


