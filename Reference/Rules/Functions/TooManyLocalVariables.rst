.. _functions-toomanylocalvariables:


.. _too-many-local-variables:

Too Many Local Variables
++++++++++++++++++++++++


.. meta::

	:description:

		Too Many Local Variables: Too many local variables were found in the methods.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Too Many Local Variables

	:twitter:description: Too Many Local Variables: Too many local variables were found in the methods

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Too Many Local Variables

	:og:type: article

	:og:description: Too many local variables were found in the methods

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Many Local Variables.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TooManyLocalVariables.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/TooManyLocalVariables.html","name":"Too Many Local Variables","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Too many local variables were found in the methods","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Many Local Variables.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Too many local variables were found in the methods. When over 15 variables are found in such a method, a violation is reported.

Local variables exclude globals (imported with global) and arguments. Local variable include `static <https://www.php.net/manual/en/language.oop5.static.php>`_ variables.

When too many variables are used in a function, it is a code smells. The function is trying to do too much and needs extra space for juggling.
Beyond 15 variables, it becomes difficult to keep track of their name and usage, leading to confusion, overwriting or hijacking.

.. code-block:: php
   
   <?php
   
   // This function is OK : 3 vars are arguments, 3 others are globals.
   function a20a3g3($a1, $a2, $a3) {
       global $a4, $a5, $a6;
       
       $a1  = 1;
       $a2  = 2;
       $a3  = 3 ;
       $a4  = 4 ;
       $a5  = 5 ;
       $a6  = 6 ;
       $a7  = 7 ;
       $a8  = 8 ;
       $a9  = 9 ;
       $a10 = 10;
       $a11  = 11;
       $a12  = 12;
       $a13  = 13 ;
       $a14  = 14 ;
       $a15  = 15 ;
       $a16  = 16 ;
       $a17  = 17 ;
       $a18  = 18 ;
       $a19  = 19 ;
       $a20 = 20;
   
   }
   
   // This function has too many variables
   function a20() {
       
       $a1  = 1;
       $a2  = 2;
       $a3  = 3 ;
       $a4  = 4 ;
       $a5  = 5 ;
       $a6  = 6 ;
       $a7  = 7 ;
       $a8  = 8 ;
       $a9  = 9 ;
       $a10 = 10;
       $a11  = 11;
       $a12  = 12;
       $a13  = 13 ;
       $a14  = 14 ;
       $a15  = 15 ;
       $a16  = 16 ;
       $a17  = 17 ;
       $a18  = 18 ;
       $a19  = 19 ;
       $a20 = 20;
   
   }
   
   ?>

+-------------------------------+---------+---------+------------------------------------------------------------------+
| Name                          | Default | Type    | Description                                                      |
+-------------------------------+---------+---------+------------------------------------------------------------------+
| tooManyLocalVariableThreshold | 15      | integer | Minimal number of variables in one function or method to report. |
+-------------------------------+---------+---------+------------------------------------------------------------------+


Connex PHP features
-------------------

  + `variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/variable.ini.html>`_
  + `local-variable <https://php-dictionary.readthedocs.io/en/latest/dictionary/local-variable.ini.html>`_
  + `scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/scope.ini.html>`_
  + `local-scope <https://php-dictionary.readthedocs.io/en/latest/dictionary/local-scope.ini.html>`_


Suggestions
___________

* Remove some of the variables, and inline them
* Break the big function into smaller ones
* Find repeated code and make it a separate function




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/TooManyLocalVariables                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.9.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-humo-gen-functions-toomanylocalvariables`                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


