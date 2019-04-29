To: DPDK Technical Board

CC: DPDK Developers Mailing List

Hi folks,

In light of the renewed community discussion on API Stability
(https://mails.dpdk.org/archives/dev/2019-April/128969.html),
now is right time to open a discussion on how DPDK is distributed and updated.

To this point in time, DPDK's primary distribution method has been as source
code distributed as a tarball from dpdk.org. This distribution method in
addition to abi instability and the dpdk's build system default behaviour of static linking
have all encouraged the "tight coupling" or "vendorization" of DPDK.

These behaviours makes it a challenge for end users, those deploying
applications based on DPDK, to manage and update DPDK in a method consistent with
other system libraries. For instance, an end user may not have any idea which
version of DPDK a consuming application may be using and if this DPDK version is reasonably up to
date with the latest upstream version. This would not be the case for other system
libraries such as glibc.

For these reasons, now is the right time for DPDK to embrace standard Operating
System practices for distributing and updating system libraries. The current industry push
towards cloud and cloud-friendliness make addressing this issue all the more timely. 

To this end, the following proposals are made for discussion at the next
techboard meeting:-

* The primary method of distributing DPDK should be as an operating system
  package, dpdk.org should be updated to reflect this reality and
  provide OS installation details in place of tarball downloads.

* DPDK should build as a dynamic shared libraries by default, to encourage loose
  coupling with consuming applications.

* Future guarantees around ABI/API stability should be provided, so that OS
  packagers can offer safe upgrade paths for consuming applications.

Thank you,

<please sign your name & role here>

Ray Kinsella, DPDK and FD.io Contributor
Luca Boccassi, Debian maintainer and DPDK LTS maintainer
