.. post:: 2024-04-02
   :author: Dale Glass

NLnet grant extended!
---------------------

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
