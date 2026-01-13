.. post:: 2024-04-16
   :author: HifiExperiments

NLnet grant extended again!
---------------------------

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
