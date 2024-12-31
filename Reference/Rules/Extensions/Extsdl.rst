.. _extensions-extsdl:

.. _ext-sdl:

ext/sdl
+++++++

.. meta\:\:
	:description:
		ext/sdl: Extensions ext/sdl.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/sdl
	:twitter:description: ext/sdl: Extensions ext/sdl
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/sdl
	:og:type: article
	:og:description: Extensions ext/sdl
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extsdl.html
	:og:locale: en
  Extensions ext/sdl.

Simple DirectMedia Layer (SDL) is a cross-platform software development library designed to provide a hardware abstraction layer for computer multimedia hardware components.

.. code-block:: php
   
   <?php
   /**
    * Example of how to change screen properties such as title, icon or state using the PHP-SDL extension.
    *
    * @author Santiago Lizardo <santiagolizardo@php.net>
    */
   require 'common.php';
   SDL_Init( SDL_INIT_VIDEO );
   $screen = SDL_SetVideoMode( 640, 480, 16, SDL_HWSURFACE );
   if( null == $screen )
   {
   	fprintf( STDERR, 'Error: %s' . PHP_EOL, SDL_GetError() );
   }
   for( $i = 3; $i > 0; $i-- )
   {
   	SDL_WM_SetCaption( "Switching to fullscreen mode in $i seconds...", null );
   	SDL_Delay( 1000 );
   }
   SDL_WM_ToggleFullscreen( $screen );
   SDL_Delay( 3000 );
   SDL_WM_ToggleFullscreen( $screen );
   SDL_WM_SetCaption( "Back from fullscreen mode. Quitting in 2 seconds...", null );
   SDL_Delay( 2000 );
   SDL_FreeSurface( $screen );
   SDL_Quit();
   
   ?>

See also `phpsdl <https://github.com/Ponup/phpsdl>`_, `Simple DirectMedia Layer <https://en.wikipedia.org/wiki/Simple_DirectMedia_Layer>`_ and `About SDL <https://www.libsdl.org/>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extsdl                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.5.6                                                                                                                                                                                   |
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


