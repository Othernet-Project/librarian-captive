=================
librarian-captive
=================

Redirects requests which are the result of an operating systems captive portal
test.

Installation
------------

The component has the following dependencies:

- librarian-core_

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

.. _librarian-core: https://github.com/Outernet-Project/librarian-core
