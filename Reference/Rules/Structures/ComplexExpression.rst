.. _structures-complexexpression:


.. _too-complex-expression:

Too Complex Expression
++++++++++++++++++++++

.. meta::
	:description:
		Too Complex Expression: Long expressions should be broken in small chunks, to limit complexity.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Too Complex Expression
	:twitter:description: Too Complex Expression: Long expressions should be broken in small chunks, to limit complexity
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Too Complex Expression
	:og:type: article
	:og:description: Long expressions should be broken in small chunks, to limit complexity
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Too Complex Expression.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComplexExpression.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/ComplexExpression.html","name":"Too Complex Expression","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Long expressions should be broken in small chunks, to limit complexity","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Too Complex Expression.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Long expressions should be broken in small chunks, to limit complexity. 

Really long expressions tends to be `error <https://www.php.net/error>`_ prone : either by typo, or by missing details. They are even harder to review, once the initially build of the expression is gone. 

As a general rule, it is recommended to keep expressions short. The analysis include any expression that is more than 15 tokens large : variable and operators counts as one, properties, arrays count as two. Parenthesis are also counted. 

PHP has no specific limit to expression size, so long expression are legal and valid. It is possible that the business logic requires a complex equation.

.. code-block:: php
   
   <?php
   
   // Why not calculate wordwrap size separatedly ? 
   $a = explode("\n", wordwrap($this->message, floor($this->width / imagefontwidth($this->fontsize)), "\n"));
   
   // Longer but easier to read
   $width = floor($this->width / imagefontwidth($this->fontsize)), "\n");
   $a = explode("\n", wordwrap($this->message, $width);
   
   // Here, some string building, including error management with @, is making the data quite complex.
   fwrite($fp, 'HEAD ' . @$url['path'] . @$url['query'] . ' HTTP/1.0' . "\r\n" . 'Host: ' . @$url['host'] . "\r\n\r\n")
   
   // Better validation of data. 
   $http_header = 'HEAD ';
   if (isset($url['path'])) {
       $http_header .= $url['path'];
   }
   if (isset($url['query'])) {
       $http_header .= $url['query'];
   }
   
   $http_header .=  "\r\n";
   if (isset($url['host'])) {
       $http_header .= 'Host: ' . $url['host'] . "\r\n\r\n";
   }
   
   fwrite($fp, $http_header);
   
   ?>

+----------------------------+---------+---------+----------------------------------------------------------+
| Name                       | Default | Type    | Description                                              |
+----------------------------+---------+---------+----------------------------------------------------------+
| complexExpressionThreshold | 30      | integer | Minimal number of operators in one expression to report. |
+----------------------------+---------+---------+----------------------------------------------------------+



Suggestions
___________

* Reduce complexity by breaking the expressions into smaller ones




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ComplexExpression                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.16                                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`multiline-expressions`                                                                                                                                                            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


