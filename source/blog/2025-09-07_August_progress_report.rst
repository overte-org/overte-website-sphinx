.. post:: 2025-09-07
   :author: Julian Groß

August progress report
----------------------

Organizational
^^^^^^^^^^^^^^

Employment
""""""""""

Last post we asked for donations in case unforeseen costs come up with my (Julian Groß) employment. As it turns out, the employment does indeed cost a little bit more (~30€) than I anticipated, costing around 1000€ per month, roughly 710€ of which actually end up on my bank account.  (I say “around” and “roughly” because most months cannot be cleanly divided by 4 weeks.)

I want to personally thank everyone who donated. Most of the people who donated appear to be new people who had never even tried Overte before donating.
I also want to specially thank our regular donators and paying Overte e.V. members, who keep Overte running. You know who you are, and you rock!

Next time, I should have the donation banner count all money paid towards the Overte e.V., instead of just extra funds on top of the regular donations minus transaction fees.
I did it this way for accounting purposes and that was probably just a bad idea.

NLnet grant
"""""""""""

In other news, the NLnet Foundation has accepted another grant (amendment) proposal from us. After having been successfully working with them for over 1 1/2 years now, it feels great to still be among all the amazing open source projects supported by them.

We want to thank NLnet and the European Commission for fostering software freedom with their Next Generation Internet programme.

Project plan
~~~~~~~~~~~~

The funding will be used to pay developers to work on the areas listed below.

Features
********

- Multi-packet avatar updates
- linear interpolation for avatar updates
- Finish multi-packet entity properties

Graphics
********

- Vulkan frame transfer to VR plugin

Maintenance
***********

- Switch to using a package lock file on Conan and updating it semi-automatically using something like Renovate
- Try getting NSIS more foolproof (boolean checks are unreliable as they only check for one possible boolean naming scheme)
- Document networking code

Bug Fixes
*********

- Fix networking congestion control ( https://github.com/overte-org/overte/issues/572#issuecomment-2799907780 )
- Fix retransmissions ignoring congestion control ( https://github.com/overte-org/overte/issues/572#issuecomment-2799907780 )

Entity Transition Shader (Fade)
*******************************

We have a special shader that makes user appear as if they were "beaming in" or "beaming out" when connecting or disconnecting. Apparently, there is unfinished support for doing this to other entities as well, which we would like to fix/finish and polish. This can be used for multiple purposes, but playing similar animations when people edit worlds, for example by deleting entities, is what got us to look into this.

- Add/fix entity transition shader
- Expose avatar and entity transition shader as zone properties
- Expose entity transition shader to Entities.addEntity and Entities.deleteEntity (overriding zone properties)

macOS support
*************

With the Vulkan PR almost merged into master, Apple getting rid of OpenGL isn't a blocker to our macOS support anymore. However, macOS support was broken for multiple years, always was on the back burner, and we moved build systems in-between, so this is a bit of a larger job. We have a good amount of macOS users who are willing to test, and even some people who are still running our last macOS version, eagerly waiting for a new one.

- Get macOS development machine
- Build with MoltenVK
- Get all of our Conan packages to build on macOS
- Fix the server software crashing on macOS
- Set up automatic macOS CI builds

Android support
***************

With the new Conan dependency manager, overhauled build system, and experience with Conan, CMake, and our build system, I now feel comfortable tackling Android support. We used to have experimental Android support, but Google changed so much of their build system API for C++ that that part needs to be completely rewritten.

- Get all of our required Conan packages to build for Android
- Add Android support to our build system
- Set up automatic Android CI builds
- Add initial OpenXR support to our Android client


Depot.dev
"""""""""

Overte got its first corporate sponsor: `Depot.dev 🔗 <https://depot.dev/?utm_source=Overte>`_ is graciously providing us with their Continuous Integration services for free.

With us needing to build Qt from source on Windows, the free GitHub hosted Runners were timing out because our builds would take over 6 hours any time there was a Qt package cache miss. So we needed a solution which didn't involve constant babysitting of the CI pipeline, which would have defeated the point of having a CI pipeline in the first place. Getting faster Runners from GitHub would have costed us upwards of 2000€ extra per year, which frankly would have broken the bank.

This is where Depot.dev comes in. Not only are they *way* cheaper than GitHub hosted Runners and provide a lot more cache space, but they also offer discounts for non-profits and open-source projects.

Interesting enough, even the same spec runners on Depot.dev are actually quite a lot faster at building Overte than the ones on GitHub already.


Progress
^^^^^^^^

Frankly speaking, so much stuff got done this month that I am having a hard time deciding what to mention.

On my side, I have spent most of my time with fixing up our Qt package for Windows and doing more build system improvements. Big thanks to 74hc595 for finding lots of additional issues in my Qt package. 😅
Together, we found out that release builds were actually building with Qt asserts enabled. Asserts are basically deliberate crashes, which exist to make us developers aware of something unexpected happening. They shouldn't be enabled in a release build, as the application often continues to function even when something we didn't expect happens.
It's quite frustrating working on something that takes three hours to build any time there is a change on an operating system you aren't usually developing on, but I am quite happy with the results.

Thanks to NLnet, I also started working on macOS support. For now, I got all the required dependencies to build and am waiting for Vulkan to be merged and our update to libnode 22 to be finished.


74hc595 did a *lot* of work as usual. They fixed multiple audio issues, helped a lot with getting Pull Requests finished, tested and merged, fixed that weird bug with people starting floating while having their camera zoomed into the back of their heads, fixed multiple crashes on Windows, … you get the idea.


Ada also did a lot of miscellaneous bug fixes, but also upstreamed their Context menu, fixed a lot of issues with VR and OpenXR, added OpenXR body tracking support, added multiple new JavaScript APIs, et cetera.
We keep merging Pull Requests and Ada keeps opening new ones.


HifiExperiments added initial VRM file format support, fixed remaining issues with his new multi-layered materials, and helped Ada and 74hc595 with graphics work as usual.


Alezia worked on improving the Snap app, added bookmarks and per-Place user counts to the Places app, and cleaned up the Places app's code.


We also got a new contributor this month: RTUnreal started work on packaging Overte for NixOS. To that end, they already added support for our build system to use only system libraries, uncovered and fixed some bugs, and have been a huge help with the libnode 22 upgrade.
Considering how many people already dabbled with trying to build Overte using Nix and gave up once they realized how much work it is going to be, it is especially great to see RTUnreal get changes merged into Overte.

Release candidate!
^^^^^^^^^^^^^^^^^^

On the topic of progress: We tagged our first release candidate since switching from VCPKG to Conan. Version 2025.09.1-rc1 and its changelog are available `here 🔗 <https://github.com/overte-org/overte/releases/tag/2025.09.1-rc1>`__ and come with a *huge* list of bug fixes, improvements, additions, and changes.
So far, this release candidate has been rock solid, so it might turn into a full release already next week without any additional changes necessary.
