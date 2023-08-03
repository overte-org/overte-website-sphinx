.. include:: shared.rst

#########
Downloads
#########

The current release candidate of Overte is version 2023.07.1-rc3.
This release includes complete replacement of script engine and a lot of other improvements. 
When used as a client 2023.07.1-rc3 is recommended over stable build 2022.12.1.
On server side 2022.12.1 is still recommended but testing and reporting bugs on 2023.07.1-rc3 is very welcome.

The current stable release of Overte is version 2022.12.1.
Take a look at the changelog on GitHub: `Changelog 🔗 <https://github.com/overte-org/overte/blob/master/CHANGELOG.md>`_


-----
Linux
-----

*********
Interface
*********

.. button-link:: https://public.overte.org/build/overte/release-candidate/2023.07.1-rc3/Overte-2023.07.1-rc3-nodebug-x86_64.AppImage
    :shadow:
    :color: primary

        Linux AppImage for amd64/x86_64 (release candidate, recommended) :octicon:`desktop-download;0.9em;`

.. button-link:: https://public.overte.org/build/overte/release/2022.12.1/Overte-2022.12.1-x86_64.AppImage
    :shadow:
    :color: primary

        Linux AppImage for amd64/x86_64 (stable version) :octicon:`desktop-download;0.9em;`

.. note::

    You will need to set the AppImage as **executable** using your file manager,
    or a command like: :bash:`chmod +x Overte.AppImage`.


*************
Domain Server
*************

Select the appropriate package for your distribution and architecture from our `GitHub Release page 🔗 <https://github.com/overte-org/overte/releases/tag/2022.12.1/>`_,
or directly from `public.overte.org 🔗 <https://public.overte.org/index.html#build/overte/release/2022.12.1/>`_.


-------
Windows
-------

The Windows installer contains both Interface and the Domain Server.
Select a custom install and tick “Overte Server” during the installation process if you want to run a Domain Server.
You can always rerun the installer later to install the server software afterwards.

.. button-link:: https://public.overte.org/build/overte/release-candidate/2023.07.1-rc3/Overte-2023.07.1-rc3.exe
    :shadow:
    :color: primary

        Windows Installer for x86_64 (release candidate, recommended for client) :octicon:`desktop-download;0.9em;`

.. button-link:: https://public.overte.org/build/overte/release/2022.12.1/Overte-2022.12.1-signed.exe
    :shadow:
    :color: primary

        Windows Installer for x86_64 (stable build, recommended for server) :octicon:`desktop-download;0.9em;`

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
