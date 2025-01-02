.. _extensions-extwasm:

.. _ext-wasm:

ext/wasm
++++++++

.. meta::
	:description:
		ext/wasm: Extension WASM.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/wasm
	:twitter:description: ext/wasm: Extension WASM
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/wasm
	:og:type: article
	:og:description: Extension WASM
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/wasm.html
	:og:locale: en
Extension WASM.

The goal of the project is to be able to run WebAssembly binaries from PHP directly. So much fun coming!

From the php-ext-wasm documentation :

.. code-block:: php
   
   <?php
   
   //There is a toy program in examples/simple.rs, written in Rust (or any other language that compiles to WASM):
   // Stored in file __DIR__ . '/simple.wasm'
   /*
   #[no_mangle]
   pub extern "C" fn sum(x: i32, y: i32) -> i32 {
       x + y
   }
   */
   
   $instance = new WASM\Instance(__DIR__ . '/simple.wasm');
   
   var_dump(
       $instance->sum(5, 37) // 42!
   );
   
   ?>

See also `php-ext-wasm <https://github.com/Hywan/php-ext-wasm>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extwasm                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.7                                                                                                                                                                                   |
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


