.. _extensions-extparle:


.. _ext-parle:

ext/parle
+++++++++


.. meta::

	:description:

		ext/parle: Extension Parser and Lexer.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/parle

	:twitter:description: ext/parle: Extension Parser and Lexer

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/parle

	:og:type: article

	:og:description: Extension Parser and Lexer

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/parle.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extparle.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extparle.html","name":"ext\/parle","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension Parser and Lexer","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/parle.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension Parser and Lexer.

The parle extension provides lexing and parsing facilities. The implementation is based on » Ben Hanson's libraries and requires a » C++14 capable compiler.

.. code-block:: php
   
   <?php
   
   use Parle\{Token, Lexer, LexerException};
   
   /* name => id */
   $token = array(
           'EOI' => 0,
           'COMMA' => 1,
           'CRLF' => 2,
           'DECIMAL' => 3,
   );
   /* id => name */
   $token_rev = array_flip($token);
   
   $lex = new Lexer;
   $lex->push("[\x2c]", $token['COMMA']);
   $lex->push("[\r][\n]", $token['CRLF']);
   $lex->push("[\d]+", $token['DECIMAL']);
   $lex->build();
   
   $in = "0,1,2\r\n3,42,5\r\n6,77,8\r\n";
   
   $lex->consume($in);
   
   do {
           $lex->advance();
           $tok = $lex->getToken();
   
           if (Token::UNKNOWN == $tok->id) {
                   throw new LexerException('Unknown token "'.$tok->value.'" at offset '.$tok->offset.'.');
           }
   
           echo 'TOKEN: ', $token_rev[$tok->id], PHP_EOL;
   } while (Token::EOI != $tok->id);
   
   ?>

See also `Parsing and Lexing <https://www.php.net/manual/en/book.parle.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extparle                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.12                                                                                                                                                                                 |
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


