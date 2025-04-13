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

----------------------------------------------
2025-04-04 We've obtained another NLnet grant!
----------------------------------------------

After the success of our previous grant, which enabled myriad fixes, improvements, and new features, we are pleased to announce that we've obtained a second NLnet grant!

The NLnet Foundation continues to support many amazing Open Source projects, and we're honored to continue partnering with them.

As with the previous grant, we commit to keeping users and developers up to date with the progress made on these items, both during our usual Saturday development meetings and on GitHub, so that everyone can follow along with the progress.


Project plan
^^^^^^^^^^^^

The funding will be used to pay developers to work on the areas listed below, with the possibility of extensions and additional work.

The agreed upon deadline for completion is December 1st, 2025.


Features
""""""""

We would like to allow less technical users to more comfortably make use of all the features
provided by our scripting engine. To that end, we would like to add a visual scripting system.

* Visual scripting (https://github.com/overte-org/overte/issues/982)
* Chat messages in 3D space (https://github.com/overte-org/overte/issues/1147)
* Add copy and paste buttons to VR keyboard (https://github.com/overte-org/overte/issues/130)
* Support OpenXR finger tracking (https://github.com/overte-org/overte/issues/224)
* Cryptography functions in scripting API (https://github.com/overte-org/overte/tree/feature/cryptography)
* Add live translation support to chat

Graphics
""""""""

Our engine uses its own internal graphics API, which is largely undocumented. Documenting this API is a lot of work and important for the future maintainability of the project. Additionally, we would like to spend more time on Vulkan optimization, especially on troubleshooting performance issues on Intel Arc graphics cards.

* Vulkan optimization
* Internal graphics API documentation
* Have local lights affect MToon materials (https://github.com/overte-org/overte/issues/1131)
* Expose normal map attenuation distance as zone property (https://github.com/overte-org/overte/issues/1139)
* Use standard physically-based-rendering for voxels (https://github.com/overte-org/overte/issues/749)
* Allow switching between graphics APIs through command line option
* Add splat mapping functionality (https://github.com/overte-org/overte/issues/1163)
* Add a no-filter texture filtering mode (https://github.com/overte-org/overte/issues/145)

QML Localization
""""""""""""""""

As Overte is used by people from all over the world, we want to add localization support. This task
aims to allow translating all internal UI created using QML. (Most, but not all, of our UI uses QML.)

* Mark strings as translatable
* Generate translation files automatically
* Hook up to Weblate translation system
* Build with translations
* Check if we include the required fonts
* Add German translation (as a reference test case)

Maintenance
"""""""""""

CMake 4.0 is around the corner, dropping support for some legacy compatibility, which seems to
break almost every one of our dependencies. Libnode has similarly received updates, including
breaking changes.

* Update Overte for CMake 4.0 compatibility
* Fix building dependencies on CMake 4.0
* Update libnode to the next LTS version
* Improve build instructions for building with KDevelop and CLion
* Add automatic Docker release builds
* Finish getting Overte into Flathub
* Update to Qt 6 (https://github.com/overte-org/overte/issues/1243)
* Package Qt 6 dependency for Windows
* Package Qt 6 dependency for Linux
* Package webrtc-audio-processing
* Switch to libdatachannel

Bug Fixes
"""""""""

* Fix MToon materials not showing up in Material Inspector (https://github.com/overte-org/overte/issues/1028)
* Text entities: show tofu character on missing character (https://github.com/overte-org/overte/issues/1133)
* Add "blocklist" for known broken graphics drivers
* Fix server Console trying to connect to highfidelity.com (https://github.com/overte-org/overte/issues/578)
* Fix QML warning message spam on Windows (https://github.com/overte-org/overte/issues/593)
* Fix problems with HifiControlsUit.SpinBox (https://github.com/overte-org/overte/issues/921)
* Fix uninstalling Overte not removing cache from AppData\Local (https://github.com/overte-org/overte/issues/952)
* Fix avatar bookmarks silently failing on broken syntax (https://github.com/overte-org/overte/issues/192)

UI Rework
"""""""""

Our current UI is a mix of different themes, design philosophies, and programming languages (https://github.com/orgs/overte-org/projects/8). Specifcally our Create app could use some
improvement (https://github.com/overte-org/overte/issues/1145).

* Framework for default QML applications
* Rework Avatar app
* Add grid shader to Create
* Allow switching Create windows between external and embedded windows
* Rework asset browser
* Rework voxel edit mode
* Allow parenting entities using drag and drop in entity list
* Add a tree view to entity list
* Add a free camera mode to Create
* Improve material management in Create
* Add centered scaling to Create
* Rework More app
* Rework settings
* Rework Pal app (People list)
* Rework log viewer
* Rework Snapshot app
* Rework Emote app
* Rework running scripts window
* Rework Places app
* Rework notifications
* Add theming support
* Prefer using system file-picker
* Add dashboard user interface

Integrate results from UX review and security audit
"""""""""""""""""""""""""""""""""""""""""""""""""""

* Perform UX review
* Perform Security audit


Thanks
""""""

* NLnet, for continuing to support Overte.
* Julian Groß, for negotiating this agreement.
* All of the developers who have agreed to take on this work.
* The Overte community, for making this possible.


--------------------------------------
2024-04-16 NLnet grant extended again!
--------------------------------------

We've obtained another extension to the NLnet grant, with the following additional items:


Maintenance
^^^^^^^^^^^

* Fix warnings and allow turning on warnings-as-errors (https://github.com/overte-org/overte/issues/930)
* Clean up Application.cpp so it's not 10,000 lines (https://github.com/overte-org/overte/issues/931)
* fix setting joint data by name (https://github.com/overte-org/overte/issues/613)
* Replace the old wearables system with avatar entities to deduplicate code. (https://github.com/overte-org/overte/issues/932)

Text entities
^^^^^^^^^^^^^

Our text entities need some love. They are clunky, and most importantly they use a custom format that isn't documented anywhere; Meaning that we cannot add new fonts, which is especially bad because the current fonts only support ASCII character.

* clip to edges instead of completely disappearing (https://github.com/overte-org/overte/issues/583)
* Switch to a standard font format (https://github.com/overte-org/overte/issues/126)

Graphics improvements II
^^^^^^^^^^^^^^^^^^^^^^^^

* Add ambient light color (https://github.com/overte-org/overte/issues/6)
* Loading MToon materials directly from glTF (https://github.com/overte-org/overte/issues/933)
* Optional camera clipping (https://github.com/overte-org/overte/issues/618)
* Custom shader fallback (https://github.com/overte-org/overte/issues/640): One fallback for if a shader fails to load/compile and one for if a user has procedural shaders disabled
* Exposing more graphics settings (tone-mapping, bloom, procedural shaders, AO) (https://github.com/overte-org/overte/issues/740, https://github.com/overte-org/overte/issues/741, https://github.com/overte-org/overte/issues/14)
* add tone-mapping and Ambient Occlusion properties to Zone entities (https://github.com/overte-org/overte/issues/934)

Miscellaneous improvements II
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

* Add VR laser smoothing which will especially help people with shaky hands (https://github.com/overte-org/overte/issues/883)
* Increase loading priority of avatar entities (https://github.com/overte-org/overte/issues/834)
* Add option to not have an avatar show until its entities are loaded (https://github.com/overte-org/overte/issues/834)
* Improve current loading priority system (https://github.com/overte-org/overte/issues/834)
* Add a property to influence load priority of entities (https://github.com/overte-org/overte/issues/834)


--------------------------------
2024-04-02 NLnet grant extended!
--------------------------------

We've obtained an extension to the NLnet grant, with the following additional items:


Linux FHS Support
^^^^^^^^^^^^^^^^^

The Linux Filesystem Hierarchy standard defines the proper file layout for an application. This work would involve adopting it, and adding some nice improvements as well.

This will:

* Make packaging easier and allow inclusion in distributions.
* Make SELinux easier.
* Allow easy instancing out of the box.
* Make Mac packaging easier.

Tasks:

* Domain server/assignment client implementation (https://github.com/overte-org/overte/issues/903)
* Interface implementation (https://github.com/overte-org/overte/issues/904)


LDAP Support
^^^^^^^^^^^^

LDAP is a common authentication mechanism, widely supported in organizations. Active Directory is compatible as well.

This will help Overte integrate much better into corporate and university structures. They could use their own internal system to control authentication. We'd save the need to write that code ourselves, which is of little interest and has been done better by other projects.

Tasks:

* Basic support in domain web UI to allow multiple users to authenticate. (https://github.com/overte-org/overte/issues/905)
* Basic support as an alternative to directory server: user accounts, domain directory. (https://github.com/overte-org/overte/issues/906)
* Full alternative to directory server. Support user relationships, data storage, profile metadata. (https://github.com/overte-org/overte/issues/907)


IPv6 Support
^^^^^^^^^^^^

IPv6 adoption is reaching quite good levels as of late, and is especially important in environments that are hurting for IPv4 addresses such as corporate, universities, cloud and large deployments.
Some providers already are charging extra for IPv4 addresses, so supporting IPv6 helps making hosting domains cheaper.

Tasks:

* Basic support in domain web UI. (https://github.com/overte-org/overte/issues/908)
* Support for fetching assets over IPv6 in interface. (https://github.com/overte-org/overte/issues/909)
* Support for domains running on IPv6. (https://github.com/overte-org/overte/issues/910)



SELinux
^^^^^^^

SELinux is a security system that allows sandboxing applications and daemons.


SELinux would sandbox the domain server and optionally the interface, to ensure that any exploits can't affect the rest of the system. For instance, a domain exploit could still break the domain, but couldn't use the server to attack other computers or expose the user's private data.

Tasks:

* Confine domain-server. (https://github.com/overte-org/overte/issues/911)
* Confine assignment clients. (https://github.com/overte-org/overte/issues/912)
* Attempt supporting multiple instances with isolation. (https://github.com/overte-org/overte/issues/913)
* Isolate multiple Overte servers on the same machine from each other. (https://github.com/overte-org/overte/issues/914)
* Confine interface. (https://github.com/overte-org/overte/issues/915)


Canvas texture
^^^^^^^^^^^^^^

This would implement a new concept of a software defined canvas texture. Scripts can draw on it, and clients receive updates.

This has a huge potential range of useful functionality:

* Software defined textures
* Script-generated nametags, banners, status displays, etc.
* Screen sharing without any external dependencies
* Whiteboard
* Synchronized web entity
* Server-side rendered web entity. This would help with the Quest implementation.

Tasks:

* Basic implementation. Texture object, simple operations like painting pixels and blocks. (https://github.com/overte-org/overte/issues/916)
* Proper canvas API. Support for fonts, graphics primitives like rectangles, circles, curves, etc. (https://github.com/overte-org/overte/issues/917)
* Screen sharing (https://github.com/overte-org/overte/issues/918)
* Synchronized web surface. (https://github.com/overte-org/overte/issues/919)


-----------------------------------------
2024-02-24 We've obtained an NLnet grant!
-----------------------------------------

The NLnet Foundation is an organization that supports many amazing Open Source projects, and we're elated to announce that we've also made the list!

As part of the agreement, we commit to keeping users and developers up to date with the progress made on these items at least every two months. For that, we'll keep track of it during our usual Saturday development meetings, and use tags, projects and other functionality on GitHub to make it easy for anyone interested to follow the progress.


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
* Finish overhauling TAA with velocity buffer (https://github.com/overte-org/overte/pull/501)
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

Build system improvements
"""""""""""""""""""""""""
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
    Code of Conduct <code_of_conduct>
    Imprint <imprint>
    Privacy policy <privacy_policy>
