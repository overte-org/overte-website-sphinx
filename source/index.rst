.. include:: shared.rst

#####
About
#####

Overte is an :ref:`open source<reference_to_downloads_source>` virtual worlds and social VR software which enables you to create and share virtual worlds as virtual reality (VR) and desktop experiences. You can create and host your own virtual world,
explore other worlds, meet and connect with other users, attend or host live VR events, and much more.

The Overte software provides the following key features:

* Collaborative world creation and editing
* VR support, including body tracking
* Scalability for up to 500 users in a single world
* Scripting in JavaScript, which allows creation of games, interactables, UI elements, and custom applications
* High quality low latency spatial audio
* Powerful physics through Bullet physics engine
* Fully open-source under the permissive Apache 2.0 license
* No central authority. You can run your own server from home.
* No user account required
* Supported by a democratic non-profit organization

:doc:`Get Overte <downloads>` |DownloadPage| or take a look at our :doc:`Gallery <gallery>` |GalleryPage|.

Join our Matrix Space on |MatrixLink| `overte:overte.org 🔗 <https://matrix.to/#/#overte:overte.org>`_.
Our Matrix Space is also bridged to |DiscordLink| `Discord 🔗 <https://discord.gg/4YuQvc8K2f>`_.

.. figure:: _images/gallery/overte-snap-by-X74hc595-on-2023-03-11_19-25-27.jpg
    :alt: Development meeting in the Overte office
    :class: inline

    Development meeting in the Overte office


####
News
####

-----------------------------------------
2024-02-24 We've obtained an NLnet grant!
-----------------------------------------

The NLnet Foundation is an organization that supports many amazing Open Source projects, and we're elated to announce that we've also made the list!

As part of the agreement, we commit to keeping users and developers up to date with the progress made on these items at least every two months. For that, we'll keep track of it during our usual Saturday development meetings, and use tags, projects and other functionality on Github to make it easy for anyone interested to follow the progress.


Project plan
^^^^^^^^^^^^

The funding will be used to pay developers that will work on the areas listed below. There exists the possibility of more work being agreed between us and NLnet.

The agreed on deadline for completion is February 17, 2025.

Some of the work has already started and can be seen on GitHub: https://github.com/overte-org/overte

Audio Overhaul
""""""""""""""


* Move audio zones to zone properties (https://github.com/overte-org/overte/issues/69)
* Add audio entities (https://github.com/overte-org/overte/issues/69)

Miscelaneous Improvements
"""""""""""""""""""""""""

* Add a wantsKeyboardFocus property for web entities (https://github.com/overte-org/overte/issues/6)
* Add interpolation on model animations (https://github.com/overte-org/overte/issues/317)

Graphics Improvements
"""""""""""""""""""""

* Fix shadow culling on back-faces (https://github.com/overte-org/overte/issues/547)
* Allow opaque particles (https://github.com/overte-org/overte/issues/776#issuecomment-1868203856)
* Finish overhaulting TAA with velocity buffer (https://github.com/overte-org/overte/pull/501)
* Add support for GPU particles

Vulkan
""""""

We're currently using OpenGL for 3D rendering. But unfortunately it's fallen out of favor in the last years, and some platforms like Mac are even deprecating it completely. AMD pays very little attention to it, and driver bugs are a frequent annoyance.

Vulkan will provide a much more modern, performant and supported renderer, and should fix our Mac support woes.

* Wireframe rendering
* Forward renderer (for low end hardware)
* Deferred renderer (fully featured)
* Optimization
* Frame transfer to VR plugin

### Build system improvements

This will make work on Overte more pleasant and make it easier to build. This is important for making maintenance easier and making life easier for future contributors.

* Switching to Conan
* Updating documentation
* Improving build process

Thanks
""""""

* NLnet, for giving us this great opportunity.
* Julian Groß, for negotiating this agreement.
* Sam Gondelman, Karol Suprynowicz and AnotherFoxGuy for taking on the work.
* The Overte community, for making this possible.




----------------------
2023-04-01 New website
----------------------

Since our old 11ty based website was unmaintained and no one knew how to edit it, we created a brand spanking new website using Sphinx, the same system that we have been using for our main documentation for years now.
This also allows us, among other things, to finally translate the website to different languages using Weblate.

If you would like to help translate this website or other parts of Overte, head over to `weblate.overte.org 🔗 <https://weblate.overte.org/>`_.


.. toctree::
    :maxdepth: 2
    :hidden:

    Home <self>
    Calendar <calendar>
    Downloads <downloads>
    Gallery <gallery>
    Contact <contact>
    Documentation 🔗 <https://docs.overte.org>
    API reference 🔗 <https://apidocs.overte.org>
    Donate <donate>
    Overte e.V. <overte_ev>
    Imprint <imprint>
    Privacy policy <privacy_policy>
