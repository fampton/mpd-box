.. _configuration:

Configuration
#############

MPD-Box use `python ConfigParser module <https://docs.python.org/2/library/configparser.html>`_ to store and read app config file.

Default configuration is saved in ``mpd_box/config.ini``.


.. code-block:: bash

	###
	# app configuration
	# http://docs.pylonsproject.org/projects/pyramid/en/1.5-branch/narr/environment.html
	###

	[mpd_box:manage]
	use = egg:mpd_box

	# TRUE FOR DEV
	pyramid.reload_templates = false
	pyramid.debug_authorization = false
	pyramid.debug_notfound = false
	pyramid.debug_routematch = false
	pyramid.default_locale_name = en

	# REMOVE FOR PROD
	pyramid.includes =
	    pyramid_debugtoolbar

	mpd_box.readers = 
		mpd_box.readers.nfc.raspberry_explorer_board

	port = 6543

	[mpd]
	# redefine MPD port
	# default : 6600
	port = 6600

	[redis]
	# redefine Redis port
	# default : 6379
	port = 6379