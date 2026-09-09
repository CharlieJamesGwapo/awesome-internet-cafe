# Awesome Internet Cafe [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of software, tools, and resources for running an internet cafe, cybercafe, gaming center, or PC bang.

Internet cafes still serve millions of users daily across Southeast Asia, Latin America, Africa, and parts of Europe. They run on a combination of billing software, time management, captive portals, diskless boot systems, and network gear — but most of this knowledge is scattered across vendor sites, forum posts, and word of mouth. This list collects what actually gets used in production.

## Contents

- [Billing & Time Management](#billing--time-management)
- [Captive Portal & Authentication](#captive-portal--authentication)
- [Network & Bandwidth Management](#network--bandwidth-management)
- [Diskless Boot & PC Cloning](#diskless-boot--pc-cloning)
- [Game Center Tools](#game-center-tools)
- [Monitoring & Statistics](#monitoring--statistics)
- [Open Source Projects](#open-source-projects)
- [Hardware](#hardware)
- [Tutorials & Guides](#tutorials--guides)
- [Communities](#communities)

## Billing & Time Management

Software that meters PC usage, charges customers, and manages prepaid time/credits.

### Commercial

- [CCBoot](https://www.ccboot.com/) — The de-facto standard for Windows-based cafes. Combines diskless boot with billing.
- [ICAFE Cloud](https://icafecloud.com/) — Cloud-managed cafe suite, popular in Asia. Includes diskless, billing, and game library.
- [Senka Cafe](https://senka.com/) — Long-running commercial billing system with strong reporting.
- [Smartlaunch](http://www.smartlaunch.net/) — Veteran billing/management platform; widely deployed in Europe.
- [MyCafeCup](http://www.mycafecup.com/) — Lightweight billing app with a free tier suitable for small cafes (up to 5 PCs).
- [HandyCafé](https://www.handycafe.com/) — Free Windows-based cafe management software with optional paid features.
- [Cafe Suite](https://www.cybexsystems.com/cafesuite.html) — Full-featured client/server billing for Windows.
- [Antamedia Internet Cafe](https://www.antamedia.com/internet-cafe-software/) — Commercial all-in-one with strong feature set.
- [Cybercafe Pro](http://www.cybercafepro.com/) — Mature platform, free for up to 4 client PCs.
- [aurora](http://auroracloud.gg/) — Fresh take on Gaming Cafe software with deep customization. Built for Windows.

### Open Source / Free

- [GLPI Cafe Plugin](https://github.com/pluginsGLPI) — Asset and ticket tracking adapted for cafe inventory.
- [phpCafeAdmin](https://sourceforge.net/projects/phpcafeadmin/) — Older PHP/MySQL billing system; useful as a reference implementation.

## Captive Portal & Authentication

Required for Wi-Fi cafes and any setup that meters per-user/voucher rather than per-PC.

- [CoovaChilli](https://coova.github.io/) — The reference open source captive portal. Pairs with FreeRADIUS.
- [FreeRADIUS](https://freeradius.org/) — The most widely deployed RADIUS server in the world. Use with daloRADIUS for a UI.
- [daloRADIUS](https://github.com/lirantal/daloradius) — Web management for FreeRADIUS — users, vouchers, hotspots, billing.
- [WiFiDog Auth Server](https://github.com/wifidog/wifidog-auth) — Mature open source captive portal still used in many embedded routers.
- [nodogsplash](https://github.com/nodogsplash/nodogsplash) — Lightweight captive portal designed for OpenWrt routers.
- [OpenNDS](https://github.com/openNDS/openNDS) — Maintained fork of nodogsplash with modern auth options.
- [PacketFence](https://github.com/inverse-inc/packetfence) — Enterprise NAC; overkill for small cafes but excellent for chains.

## Network & Bandwidth Management

The router and shaping layer beneath everything else.

- [MikroTik RouterOS](https://mikrotik.com/software) — Used in the vast majority of cafes worldwide. Hotspot, queues, RADIUS client all built in.
- [pfSense](https://www.pfsense.org/) — Free open source router/firewall on FreeBSD with captive portal support.
- [OPNsense](https://opnsense.org/) — pfSense fork with a more modern UI and faster release cadence.
- [OpenWrt](https://openwrt.org/) — Linux for embedded routers; runs nodogsplash, OpenNDS, and most captive portal stacks.
- [VyOS](https://vyos.io/) — CLI-driven routing OS; great for multi-site cafe chains.

## Diskless Boot & PC Cloning

Run all client PCs from one server image — eliminates per-PC maintenance, malware persistence, and cheating in game centers.

- [CCBoot](https://www.ccboot.com/) — Industry standard. iSCSI/PXE diskless boot for Windows clients.
- [iVentoy](https://www.iventoy.com/) — Free cross-platform PXE server; supports Windows and Linux images from one boot menu.
- [iPXE](https://ipxe.org/) — Open source network boot firmware; the foundation under many commercial diskless products.
- [LTSP (Linux Terminal Server Project)](https://ltsp.org/) — The classic Linux-side diskless solution, still actively developed.
- [FOG Project](https://fogproject.org/) — Free open source imaging/cloning solution; used to mass-deploy cafe PC images.
- [Clonezilla](https://clonezilla.org/) — Disk imaging for offline cloning workflows.

## Game Center Tools

For PC bangs, e-sports lounges, and gaming-focused cafes.

- [GGLeap](https://www.ggleap.com/) — Cloud-based esports center management; popular in NA/EU.
- [SENET](https://senet.cloud/) — Esports center platform with player profiles, tournaments, billing.
- [aurora](http://auroracloud.gg/) — Fresh take on Gaming Cafe software with deep customization. Built for Windows.
- [Open Games Library](https://github.com/openblockchainsoftware) — Community-maintained metadata for cafe game collections.
- [Steam Family Sharing](https://store.steampowered.com/promotion/familysharing) — How most cafes legally share PC game libraries across machines.
- [Lutris](https://lutris.net/) — Open source game launcher useful in Linux gaming cafes.
- [Sunshine](https://github.com/LizardByte/Sunshine) + [Moonlight](https://moonlight-stream.org/) — Open source self-hosted game streaming, increasingly used to centralize GPUs.

## Monitoring & Statistics

Know which machines are up, who's using how much bandwidth, and when peak hours happen.

- [LibreNMS](https://www.librenms.org/) — Open source network monitoring; auto-discovers MikroTik and most cafe hardware.
- [Zabbix](https://www.zabbix.com/) — Heavyweight monitoring; great for chains of 5+ branches.
- [Grafana](https://grafana.com/) + [Prometheus](https://prometheus.io/) — The modern stack for custom dashboards (peak hours, revenue per PC, etc.).
- [SmokePing](https://oss.oetiker.ch/smokeping/) — Latency monitoring; essential for game cafes and ISP uptime claims.
- [Netdata](https://github.com/netdata/netdata) — Per-host real-time metrics with zero config.
- [The Dude](https://mikrotik.com/thedude) — MikroTik's free network monitoring tool; lightweight and cafe-friendly.

## Open Source Projects

End-to-end open source stacks worth studying or contributing to.

- [OpenSplash](https://github.com/dougbtv/opensplash) — Reference open source captive portal implementation.
- [pfsense-captive-portal](https://github.com/pfsense/FreeBSD-ports) — pfSense's open captive portal source.
- [PiHole](https://pi-hole.net/) — Not cafe-specific, but commonly deployed at the edge of cafe networks for ad/malware filtering.
- [AdGuard Home](https://github.com/AdguardTeam/AdGuardHome) — Alternative to PiHole with a nicer UI; good for content filtering in family-oriented cafes.

## Hardware

Reference hardware that survives cafe environments (24/7 uptime, dust, power swings, kids).

- **Routers**: MikroTik hAP ax² and CCR2004 series for small to mid cafes; CCR2216 for chains.
- **Switches**: MikroTik CRS3xx series, TP-Link TL-SG10xx, Ubiquiti UniFi for managed setups.
- **Servers**: Refurbished Dell PowerEdge R730/R740 for diskless boot; 64GB+ RAM recommended for Windows clients.
- **UPS**: APC Smart-UPS 1500VA minimum per rack; cafes lose data more often to brownouts than crashes.
- **Peripherals**: Logitech G203/G102 mice and Redragon K552 keyboards survive heavy use at low cost.

## Tutorials & Guides

- [MikroTik Hotspot Setup Guide](https://help.mikrotik.com/docs/spaces/ROS/pages/8978449/HotSpot) — Official documentation; the canonical reference.
- [r/mikrotik wiki](https://www.reddit.com/r/mikrotik/wiki/index/) — Community wiki with cafe-relevant configs.
- [Setting up CoovaChilli + FreeRADIUS](https://wiki.freeradius.org/guide/coovachilli-howto) — Hotspot recipe for self-hosted cafes.
- [Diskless Boot 101](https://www.ccboot.com/diskless-boot.htm) — Vendor overview but technically accurate.
- [PC Bang Operations Manual (Korean)](https://namu.wiki/w/PC%EB%B0%A9) — Comprehensive Korean-language reference on PC bang operations.

## Communities

- [r/cybercafe](https://www.reddit.com/r/cybercafe/) — Operator-focused subreddit.
- [r/PCbangs](https://www.reddit.com/r/PCbangs/) — Gaming cafe operator community.
- [r/mikrotik](https://www.reddit.com/r/mikrotik/) — Network gear discussion; many cafe operators.
- [r/HomeNetworking](https://www.reddit.com/r/HomeNetworking/) — Adjacent community with cafe-relevant networking advice.
- [MikroTik Forum](https://forum.mikrotik.com/) — Vendor forum; hotspot subforum is cafe-relevant.

## Contributing

Contributions are welcome. Please read the [contribution guidelines](contributing.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Charlie James Zapico Abejo](https://github.com/CharlieJamesGwapo) has waived all copyright and related or neighboring rights to this work.
