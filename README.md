# JamNNTPd (updated version)

JamNNTPd is an NNTP server that allows newsreaders to access a JAM messagebase. It can be used to read and write messages in Fidonet/FTN echomail and netmail.

Originally created by Johan Billing, it was later maintained by Robert James Clay, with contributions by Peter Krefting and others.

This fork includes several fixes and improvements (while trying to maintain backwards compatibility).

Carlos Navarro (@cnb), Fidonet 2:341/234 (ex 2:346/3)

Check the original documentation for JamNNTPd 1.3: [ReadMe.txt](ReadMe.txt)

## Changelog

Version 1.4-c (beta)

- New `-def_squote` setting (user parameter `squote`).
  Default setting for reformatting quoted text to fidonet style. `smartquote` must not be enabled.

- New `-note` config setting.
  Insert NOTE kludge with X-Newsreader/User-Agent string

- New `-def_addcr` setting (user parameter `addcr`).
  Default setting for adding a CR (empty line) at end of message text

- New `-loggroups` setting.
  Write groups selected by users to the logfile

- Fixed: "Re:" not removed from empty subjects

- New setting `-def_nonbsp` (user parameter `nonbsp`).
  Default setting for replacing non-breaking spaces by regular spaces (UTF-8 and iso-8859-1/LATIN-1)

- New setting `-def_delssq` (user parameter `delssq`)
  Default setting for deleting stuffed space stuffing quoted text (only in format=flowed)

Version 1.3.5-c 
- prevent issues when there is no FTN origin address, e.g. local areas. Thunderbird may show incorrect From's in headers. (SmapiNNTPd had already fixed this.)

Version 1.3.4-c
- fix issues with lines starting with a dot

Version 1.3.3-c
- fix text and header corruption issues

Version 1.3.2-c
- MODE READER patch: some newsreaders don't like response 500

Version 1.3.1-c
- fix level for CHRS: UTF-8
- use server version for PID kludge

