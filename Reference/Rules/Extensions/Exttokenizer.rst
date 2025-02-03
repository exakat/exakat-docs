.. _extensions-exttokenizer:


.. _ext-tokenizer:

ext/tokenizer
+++++++++++++

.. meta::
	:description:
		ext/tokenizer: Extension Tokenizer.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/tokenizer
	:twitter:description: ext/tokenizer: Extension Tokenizer
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/tokenizer
	:og:type: article
	:og:description: Extension Tokenizer
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/tokenizer.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exttokenizer.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Exttokenizer.html","name":"ext\/tokenizer","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Tokenizer","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/tokenizer.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension Tokenizer.

The Tokenizer functions provide an interface to the PHP tokenizer embedded in the Zend `Engine <https://www.php.net/engine>`_.

.. code-block:: php
   
   <?php
   /*
   * T_ML_COMMENT does not exist in PHP 5.
   * The following three lines define it in order to
   * preserve backwards compatibility.
   *
   * The next two lines define the PHP 5 only T_DOC_COMMENT,
   * which we will mask as T_ML_COMMENT for PHP 4.
   */
   if (!defined('T_ML_COMMENT')) {
      define('T_ML_COMMENT', T_COMMENT);
   } else {
      define('T_DOC_COMMENT', T_ML_COMMENT);
   }
   
   $source = file_get_contents('example.php');
   $tokens = token_get_all($source);
   
   foreach ($tokens as $token) {
      if (is_string($token)) {
          // simple 1-character token
          echo $token;
      } else {
          // token array
          list($id, $text) = $token;
   
          switch ($id) { 
              case T_COMMENT: 
              case T_ML_COMMENT: // we\'ve defined this
              case T_DOC_COMMENT: // and this
                  // no action on comments
                  break;
   
              default:
                  // anything else -> output 'as is'
                  echo $text;
                  break;
          }
      }
   }
   ?>

See also `tokenizer <http://www.php.net/tokenizer>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Exttokenizer                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


