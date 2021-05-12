# Note from Sam Trenholme

This is a maintenance-only fork of N-DJBDNS.  The only things that
will be updated are:

* The list of root servers.
* Any security holes which are found in the future.  While I will consider
  all security reports, security holes without CVE numbers may very well
  be ignored or not patched.  
* Compile time errors in a LTS release of Ubuntu.

Other issues will not be fixed, e.g. compile-time warnings, issues in any
Linux distribution *besides* Ubuntu LTS, usability issues, etc.

My ability to support N-DJBDNS is very limited; I actually use (actually, I
*wrote*) MaraDNS, and I am only maintaining this branch of djbdns
because it’s important to have a currently maintained version of this
DNS server, and no one else is stepping up to the plate to maintain it.

# Autoconf rant

The various autoconf files here did not work with the Ubuntu 20.04 default
version of autoconf.  It would appear that autoconf is not very good about
keeping compatibility between versions, and the autoconf files were for an
older version of autoconf.

That in mind, I have replaced the autoconf input files with the
autoconf-generated files from the (probably) final N-DJBDNS release: 
`configure`, and various `Makefile.in` files.

These work on Ubuntu 20.04: A git checkout now compiles.  

New-DJBDNS
==========


Hello all,

I am pleased to release this *new* djbdns version 1.06. Djbdns is a
fully-fledged Domain Name System(DNS), originally written by the eminent
author of qmail, Dr. D J Bernstein. This new release is a complete makeover to
the original source(djbdns-1.05) and is meant to make life a lot more pleasant.
The original source is in public-domain since late Dec 2007.

Please see: http://cr.yp.to/distributors.html

Nevertheless, this new release is distributed under the GNU General Public
Licence for good. See ChangeLog for more details.

Installation:
-------------

To install djbdns, say:

    sh>$ ./configure [ --prefix=/usr/local ]
    sh>$ make
    sh># make install

Once installed, on Linux machines add `dnscache' to the system services by
following steps. Note that, if you chose a different install prefix with
`--prefix', use that instead of the default - /usr/local.

    sh># mv /usr/local/bin/dnscached /etc/init.d/dnscached
    sh># chkconfig --add dnscached
    sh># chkconfig --list dnscached

Now you can start the service by

    sh># service dnscached start

OR

    sh># dnscache -D

Consult the dnscache(8) manual page for more help.

Problems:
---------

If you encounter any problems while installing New-DJBDNS OR find bugs in its
working, please send an email to <pj.pandit@yahoo.co.in> describing in detail
about the problem/bug.

Thank you!
