.. _variables-closenaming:

.. _confusing-names:

Confusing Names
+++++++++++++++

.. meta::
	:description:
		Confusing Names: The following variables's name are very close and may lead to confusion.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Confusing Names
	:twitter:description: Confusing Names: The following variables's name are very close and may lead to confusion
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Confusing Names
	:og:type: article
	:og:description: The following variables's name are very close and may lead to confusion
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Confusing Names.html
	:og:locale: en
The following variables's name are very close and may lead to confusion.

Variables are 3 letters long (at least). Variables names build with an extra ``s`` are omitted.
Variables may be scattered across the code, or close to each other. 

Variables which differ only by case, or by punctuation or by numbers are reported here.

.. code-block:: php
   
   <?php
   
       // Variable names with one letter difference
       $fWScale = 1;
       $fHScale = 1;
       $fScale = 2;
       
       $oFrame = 3;
       $iFrame = new Foo();
       
       $v2_norm = array();
       $v1_norm = 'string';
       
       $exept11 = 1;
       $exept10 = 2;
       $exept8 = 3;
       
       // Variables that differ by punctation
       $locale = 'fr';
       $_locate = 'en';
   
       // Variables that differ by numbers
       $x11 = 'a';
       $x12 = 'b';
   
       // Variables that differ by numbers
       $songMP3 = 'a';
       $Songmp3 = 'b';
       
       // This even looks like a typo
       $privileges  = 1;
       $privilieges = true;
       
       // This is not reported : Adding extra s is tolerated.
       $rows[] = $row;
       
   ?>

See also `How to pick bad function and variable names <http://mojones.net/how-to-pick-bad-function-and-variable-names.html>`_.

Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `semantics <https://php-dictionary.readthedocs.io/en/latest/dictionary/semantics.ini.html>`_


Suggestions
___________

* Rename the variables




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Variables/CloseNaming                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


