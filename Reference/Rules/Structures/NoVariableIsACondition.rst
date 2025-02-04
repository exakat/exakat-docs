.. _structures-novariableisacondition:


.. _variable-is-not-a-condition:

Variable Is Not A Condition
+++++++++++++++++++++++++++

.. meta::
	:description:
		Variable Is Not A Condition: Avoid using a lone variable as a condition.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Variable Is Not A Condition
	:twitter:description: Variable Is Not A Condition: Avoid using a lone variable as a condition
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Variable Is Not A Condition
	:og:type: article
	:og:description: Avoid using a lone variable as a condition
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Variable Is Not A Condition.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoVariableIsACondition.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoVariableIsACondition.html","name":"Variable Is Not A Condition","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using a lone variable as a condition","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Variable Is Not A Condition.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using a lone variable as a condition. It is recommended to use a comparative value, or one of the filtering function, such as `isset() <https://www.www.php.net/isset>`_, empty(). 

Using the raw variable as a condition blurs the difference between an undefined variable and an empty value. By using an explicit comparison or validation function, it is easier to understand what the variable stands for.
Thanks to the `PMB <https://www.sigb.net/>`_ team for the inspiration.

.. code-block:: php
   
   <?php
   
   if (isset($error)) {
       echo 'Found one error : '.$error!;
   }
   
   //
   if ($errors) {
       print count($errors).' errors found : '.join('', $errors).PHP_EOL;
       echo 'Not found';
   }
   
   ?>
Connex PHP features
-------------------

  + `Comparison <https://php-dictionary.readthedocs.io/en/latest/dictionary/comparison.ini.html>`_
  + `Iffectation <https://php-dictionary.readthedocs.io/en/latest/dictionary/iffectation.ini.html>`_


Suggestions
___________

* Make the validation explicit, by using a comparison operator, or one of the validation function.




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoVariableIsACondition                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.6.5                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


