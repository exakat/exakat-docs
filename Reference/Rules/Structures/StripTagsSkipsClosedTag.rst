.. _structures-striptagsskipsclosedtag:

.. _strip\_tags()-skips-closed-tag:

strip_tags() Skips Closed Tag
+++++++++++++++++++++++++++++

.. meta\:\:
	:description:
		strip_tags() Skips Closed Tag: strip_tags() skips non-self closing tags.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: strip_tags() Skips Closed Tag
	:twitter:description: strip_tags() Skips Closed Tag: strip_tags() skips non-self closing tags
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: strip_tags() Skips Closed Tag
	:og:type: article
	:og:description: strip_tags() skips non-self closing tags
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/StripTagsSkipsClosedTag.html
	:og:locale: en
  `strip_tags() <https://www.php.net/strip_tags>`_ skips non-`self <https://www.php.net/manual/en/language.oop5.paamayim-nekudotayim.php>`_ closing tags. This means that tags such as ``<br />`` will be ignored from the second argument of the function.

.. code-block:: php
   
   <?php
   
   $input = 'a<br />';
   
   // Displays 'a' and clean the tag
   echo strip_tags($input, '<br>');
   
   // Displays 'a<br />' and skips the allowed tag
   echo strip_tags($input, '<br/>');
   
   ?>

See also `strip_tags <https://www.php.net/manual/en/function.strip-tags.php>`_.


Suggestions
___________

* Do not use self-closing tags in the second parameter




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/StripTagsSkipsClosedTag                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.3                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


