.. _extensions-extnewt:


.. _ext-newt:

ext/newt
++++++++

.. meta::
	:description:
		ext/newt: Newt PHP CLI extension.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/newt
	:twitter:description: ext/newt: Newt PHP CLI extension
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/newt
	:og:type: article
	:og:description: Newt PHP CLI extension
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/newt.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extnewt.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extnewt.html","name":"ext\/newt","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Newt PHP CLI extension","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/newt.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Newt PHP CLI extension.

This is a PHP language extension for RedHat Newt library, a terminal-based window and widget library for writing applications with user friendly interface.

.. code-block:: php
   
   <?php
   newt_init ();
   newt_cls ();
   
   newt_draw_root_text (0, 0, "Test Mode Setup Utility 1.12");
   newt_push_help_line (null);
   
   newt_get_screen_size ($rows, $cols);
   
   newt_open_window ($rows/2-17, $cols/2-10, 34, 17, "Choose a Tool");
   
   $form = newt_form ();
   
   $list = newt_listbox (3, 2, 10);
   
   foreach (array (
       "Authentication configuration",
       "Firewall configuration",
       "Mouse configuration",
       "Network configuration",
       "Printer configuration",
       "System services") as $l_item)
   {
       newt_listbox_add_entry ($list, $l_item, $l_item);
   }
   
   $b1 = newt_button (5, 12, "Run Tool");
   $b2 = newt_button (21, 12, "Quit");
   
   newt_form_add_component ($form, $list);
   newt_form_add_components ($form, array($b1, $b2));
   
   newt_refresh ();
   newt_run_form ($form);
   
   newt_pop_window ();
   newt_pop_help_line ();
   newt_finished ();
   newt_form_destroy ($form);
   ?>

See also `Newt <http://people.redhat.com/rjones/ocaml-newt/html/Newt.html>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extnewt                                                                                                                                                                      |
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


