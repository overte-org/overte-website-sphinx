.. post:: 2025-04-04
   :author: Dale Glass

We've obtained another NLnet grant!
-----------------------------------

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

Our current UI is a mix of different themes, design philosophies, and programming languages (https://github.com/orgs/overte-org/projects/8). Specifically our Create app could use some
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
