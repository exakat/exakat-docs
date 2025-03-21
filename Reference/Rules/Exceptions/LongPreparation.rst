.. _exceptions-longpreparation:


.. _long-preparation-for-throw:

Long Preparation For Throw
++++++++++++++++++++++++++

.. meta::
	:description:
		Long Preparation For Throw: When throwing an exception, move the preparing code in the exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Long Preparation For Throw
	:twitter:description: Long Preparation For Throw: When throwing an exception, move the preparing code in the exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Long Preparation For Throw
	:og:type: article
	:og:description: When throwing an exception, move the preparing code in the exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Long Preparation For Throw.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/LongPreparation.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/LongPreparation.html","name":"Long Preparation For Throw","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"When throwing an exception, move the preparing code in the exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Long Preparation For Throw.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

When throwing an `exception <https://www.php.net/exception>`_, move the preparing code in the `exception <https://www.php.net/exception>`_. This will keep the ``throw`` call simple.

.. code-block:: php
   
   <?php
   
   // Examples extracted from Alain Schlesser's blog
   public function render( $view ): string {
    
      if ( ! $this->views->has( $view ) ) {
         switch ( gettype( $view ) ) {
            case 'object':
               $view = get_class( $view );
            case 'string':
               $message = sprintf(
                  'The requested View "%s" does not exist.',
                  $view
               );
               break;
            default:
               $message = sprintf(
                  'An unknown View type of "%s" was requested.',
                  $view
               );
         }
    
         throw new ViewWasNotFound( $message );
      }
    
      echo $this->views->get( $view )
                ->render();
   }
   
   ?>

+----------------------+---------+---------+-------------------------------------------+
| Name                 | Default | Type    | Description                               |
+----------------------+---------+---------+-------------------------------------------+
| preparationLineCount | 8       | integer | Minimal number of lines before the throw. |
+----------------------+---------+---------+-------------------------------------------+



See also `Structuring PHP Exceptions session <https://phpconference.com/blog/structuring-php-exceptions/>`_ and `Best practices for handling exceptional behavior <https://www.nikolaposa.in.rs/blog/2016/08/17/exceptional-behavior-best-practices/>`_.

Connex PHP features
-------------------

  + `throw <https://php-dictionary.readthedocs.io/en/latest/dictionary/throw.ini.html>`_
  + `Exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Move the preparation into the Exception to keep the throw simple




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/LongPreparation                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.2.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


