.. post:: 2024-02-24
   :author: Dale Glass

We've obtained an NLnet grant!
------------------------------

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
