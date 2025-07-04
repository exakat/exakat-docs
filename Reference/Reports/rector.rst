.. _report-rector:

Rector
++++++

Rector
______

.. meta::
	:description:
		Rector: Suggest configuration for Rector refactoring tool..
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Rector
	:twitter:description: Rector: Suggest configuration for Rector refactoring tool.
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Rector
	:og:type: article
	:og:description: Suggest configuration for Rector refactoring tool.
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Reports/.html
	:og:locale: en

Suggest configuration for Rector refactoring tool.

The Rector report is a helper report for `Tomas Votruba <https://twitter.com/VotrubaT>`_'s `Rector <https://getrector.org/>`_ tool.

Some issues spotted by Exakat may be fixed automagically by Rector. Rector offers more than 550 (and counting) rules, that may save countless hours of work. 

For example, `CombinedAssignRector <https://github.com/rectorphp/rector/blob/master/docs/AllRectorsOverview.md#combinedassignrector>`_, simplifies ``$value = $value + 5`` into ``+$value += 5;``. On Exakat, the rule `Structures/CouldUseShortAssignation <(https://exakat.readthedocs.io/en/latest/Rules.html#could-use-short-assignation>`_ spot those too.

Not all exakat rules are covered by Rector, and vice-versa. `CompactToVariablesRector <https://github.com/rectorphp/rector/blob/master/docs/AllRectorsOverview.md#compacttovariablesrector>`_ aims at skipping usage of compact(), while `Structures/CouldUseCompact <https://exakat.readthedocs.io/en/latest/Rules.html#could-use-compact>`_ suggest the contrary. 

Rector and Exakat both use different approaches to code review. It is recommended to review the changes before committing them.

Check `RectorPHP <https://getrector.org/>`_ website, its `rector github <https://github.com/rectorphp/rector>`_ repository, and `Tomas Votruba <https://twitter.com/VotrubaT>`_ account.




::

    # Add this to your rector.yaml file
    # At the root of the source to be analyzed
    # Generated on 2021-10-14 04:15:14, by Exakat (2.2.3- build 1255)
    
    services:
        Rector\CodeQuality\Rector\If_\ShortenElseIfR
        Rector\CodeQuality\Rector\Concat\JoinStringConcatRector
    

Specs
_____

+--------------+------------------------------------------------------------------+
| Short name   | Rector                                                           |
+--------------+------------------------------------------------------------------+
| Rulesets     | Rector.                                                          |
+--------------+------------------------------------------------------------------+
| Type         | Text                                                             |
+--------------+------------------------------------------------------------------+
| Target       | This report is written in 'rector.exakat.yaml'.                  |
+--------------+------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_ |
+--------------+------------------------------------------------------------------+


