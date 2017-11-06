Oslo.policy

**Status**: Draft/Ready for Review/Reviewed
**Release**: Pike
**Version**: 1.29.1

Contacts:
PTL: name - irc handle
Architect: name - irc handle
Security Reviewer: name - irc handle

Project description and purpose
~~~~~~~~~~~~~~~~~~~~~~~~~~~
Oslo.policy is an Openstack library that provides support for Role Based Access Control (RBAC) policy enforcement
across all OpenStack services. Whenever an API call to an OpenStack service is made, the service’s policy engine uses
the appropriate policy definitions to determine if the call can be accepted. [0]

Primary users and use-cases
~~~~~~~~~~~~~~~~~~~~~~~~~
The primary users of Oslo.policy are each Openstack service such as Compute, Identity, and Networking, which each have
their own role-based access policies. When API calls to these services are made, the policy engine is used as a check
to determine whether or not the call will be accepted. Oslo.policy is a method for services to determine which users
can access which objects in what way. [0]

External dependencies & associated security assumptions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A policy file can be generated to show the registered defaults and policies loaded from a file. From a security
standpoint, one can view all effective policies that are in place. [1]


Components
~~~~~~~~~~~~~~~~
-Policy.yaml
-Policy.JSON(old version, format still supported)
-Oslo.config




RESOURCES:
~~~~~~~~~~~
[0] https://docs.openstack.org/oslo.policy/latest/admin/policy-yaml-file.html
[1] https://docs.openstack.org/oslo.policy/latest/user/usage.html#migrating-to-oslo-policy
[2]