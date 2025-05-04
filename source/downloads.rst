.. include:: shared.rst

#########
Downloads
#########

The current release of Overte is version 666.66.6.
This is a small bug fix release, mainly fixing VR startup issues in Windows.

Take a look at the changelog on GitHub: `Changelog 🔗 <https://github.com/overte-org/overte/blob/master/CHANGELOG.md>`_


-----
Linux
-----

*********
Interface
*********

.. button-link:: https://public.overte.org/build/overte/release/2025.03.3/Overte-2025.03.3-x86_64.AppImage
    :shadow:
    :color: primary

        Linux AppImage for amd64/x86_64 :octicon:`desktop-download;0.9em;`

.. note::

    You will need to set the AppImage as **executable** using your file manager,
    or a command like: :bash:`chmod +x Overte.AppImage`.


*************
Domain Server
*************

Select the appropriate package for your distribution and architecture from `public.overte.org 🔗 <https://public.overte.org/index.html#build/overte/release/2025.03.3/>`_.

There are also Docker images available on `hub.docker.com 🔗 <https://hub.docker.com/r/overte/overte-server/tags>`_. These images are still new, so please report any issues you run into on our `GitHub issue tracker 🔗 <https://github.com/overte-org/overte/issues>`_.


-------
Windows
-------

The Windows installer contains both Interface and the Domain Server.
Select a custom install and tick “Overte Server” during the installation process if you want to run a Domain Server.
You can always rerun the installer later to install the server software afterwards.

.. button-link:: https://public.overte.org/build/overte/release/2025.03.3/Overte-2025.03.3.exe
    :shadow:
    :color: primary

        Windows Installer for x86_64 :octicon:`desktop-download;0.9em;`

.. note::

    Windows Defender might display a warning about the Windows installer being potentially unsafe.
    To run it anyway click on "**More info**" and then "**Run anyway**".


.. _reference_to_downloads_source:

------
Source
------

Our source code is available on `our GitHub repository 🔗 <https://github.com/overte-org/overte/>`_.
If you intend to build from source, we would suggest building the master branch directly instead of a release, to profit from the latest improvements.

For Linux there is a helper application available that aims to simplify the build process for newcomers. Get it from GitHub here: `Overte builder 🔗 <https://github.com/overte-org/overte-builder/>`_
