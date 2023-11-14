# Status Of Services

???- bug "Scheduled maintenance"

     | Date        | Time interval    | Note                                        |
     |:------------|:----------------:|:-------------------------------------------:|
     | 20.12.2023.2023.2023  |05:30 - 6:30 EET  | **XMPP** service interruptions are possible |

## Account Registrations

| Тype              |Rate Limit              |Status                           |
|:------------------|:----------------------:|-------------------------:|
| Online            |One per hour            |![Registration Status](https://uptime.tinyserver.eu/api/badge/141/status?label=&upLabel=OPEN&downLabel=CLOSED) |
| Installed Client  |One per hour from an IP |![Registration Status](https://uptime.tinyserver.eu/api/badge/141/status?label=&upLabel=OPEN&downLabel=CLOSED) |

## Accessibility - **XMPP**

| Indicator |Value |
|:---------------------------|:---------------------------------------------------:|
| Average ping for the last 24 hours|![Ping Average](https://uptime.tinyserver.eu/api/badge/120/ping?label=) |
| Uptime for the last 24 hours |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/121/uptime/24?label=)|
| Uptime for the last 7 days |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/121/uptime/168?label=)|
| Uptime for the last 30 days |![Uptime 7 days](https://uptime.tinyserver.eu/api/badge/121/uptime/720?label=)|

## Compliance and Compatibility - **XMPP**

| Test                |Result                                                                  |
|:--------------------|-----------------------------------------------------------------------:|
| **XMPP** Compliance| ![Compliance Test](https://compliance.conversations.im/badge/chatrix.one) |
|**SRV** Records / Access| <a href='https://xmpp.love/servers/chatrix.one/results'><img src='https://xmpp.love/servers/chatrix.one/badge' width='201px' height= '18px' alt='xmpp.love score'></a> |

## Accessibility - Website

| Indicator                  | Value                                                 |
|:---------------------------|:-----------------------------------------------------:|
| Average ping for the last 24 hours|![Ping Average](https://uptime.tinyserver.eu/api/badge/135/ping) |
| Uptime for the last 24 hours |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/135/uptime/24?label=)|
| Uptime for the last 7 days |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/135/uptime/168?label=)|
| Uptime for the last 30 days |![Uptime 24h](https://uptime.tinyserver.eu/api/badge/135/uptime/720?label=)|

## Technical data

### XMPP Server

| Parameter           | Value                 |
|:--------------------|:-------------------------------:|
| Processor       | ARM Ampere    |
| RAM | 12GB |
| Disk Space | 64GB |
| File System | ext4 |
| Operating System | Ubuntu 22.04 (Jammy Jellyfish) |
| Ejabberd version | 23.1.0 |
| Backup | Weekly |
| Location | Switzerland |

### Backup server

| Parameter | Value |
|:--------------------|:-------------------------------:|
| Processor | AMD EPYC 3251 |
| RAM | 64GB |
| Disk Space | 5TB |
| File System | ZFS (RAIDZ-1) |
| Operating System | Debian 12 (Bookworm) |
| Location | Bulgaria |

## Information about occurred incidents

!!! abstract "Incidents"

     There are currently no documented incidents.

## Update history

### 14.11.2023

#### Updated Ejabberd to version [23.10](https://github.com/processone/ejabberd/releases/tag/23.10)

- Added support for XEP-0402: PEP Native Bookmarks, which is a significant improvement over XEP-0048: Bookmark Storage. Defines how bookmarks are stored.
- New: `mod_muc_occupantid` with support for XEP-0421: Occupant Id. Used for MUC anonymous rooms, fixing messages and withdrawing messages. Currently, the only client found to support XEP-0421 is Dino - version 0.4 and above.
- Many new options and features. For more information, see the official article on the [ProcessOne](https://www.process-one.net/) web site about what's new in version [23.10](https://www.process-one.net/blog/ejabberd-23-10/)

### 26.04.2023

#### Updated Ejabberd to version [23.04](https://github.com/processone/ejabberd/releases/tag/23.04)

- Many improvements in SQL databases
- New: `mod_mam` support for [XEP-0425: Message Moderation](https://xmpp.org/extensions/xep-0425.html)
- New: `mod_muc_rtbl` support for **Real-Time Block List for MUC rooms**

### 20.01.2023

#### Updated Ejabberd to version [23.01](https://github.com/processone/ejabberd/releases/tag/23.01)

- New: Registrations are open, using the online form or an installed client, protected by a **CAPTCHA** challenge

### 30.10.2022

#### Updated Ejabberd to version [22.10](https://github.com/processone/ejabberd/releases/tag/22.10)
