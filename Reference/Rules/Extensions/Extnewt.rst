.. _extensions-extnewt:

.. _ext-newt:

ext/newt
++++++++

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
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`                                                                                                      |
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


