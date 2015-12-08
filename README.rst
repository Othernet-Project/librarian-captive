=================
librarian-captive
=================

Redirects requests which are the result of an operating systems captive portal
test.

Installation
------------

The component has the following dependencies:

- librarian_core_

To enable this component, add it to the list of components in librarian_'s
`config.ini` file, e.g.::

    [app]
    +components =
        librarian_captive

Configuration
-------------

``captive_portal.domains``
    A list of ``domain:template name;status code`` entries. If a captive portal
    domain is matched from the list, a response with the specified status code
    and / or template will be returned. Example::

        [captive_portal]
        domains =
            www.apple.com:apple;200
            captive.apple.com:apple;200
            www.msftncsi.com:;302
            go.microsoft.com:;302

Development
-----------

In order to recompile static assets, make sure that compass_ and coffeescript_
are installed on your system. To perform a one-time recompilation, execute::

    make recompile

To enable the filesystem watcher and perform automatic recompilation on changes,
use::

    make watch

.. _librarian: https://github.com/Outernet-Project/librarian
.. _librarian_core: https://github.com/Outernet-Project/librarian-core
.. _compass: http://compass-style.org/
.. _coffeescript: http://coffeescript.org/
