# jellyfin-media-server-home-lab-project
This project documents the installation, configuration, and evaluation of Jellyfin, a free, open-source media server deployed on my home Windows server as a direct alternative to Plex Media Server. The core motivation was to assess whether an open-source solution could match or exceed Plex's features without the cost of a Plex Pass subscription.
🎬 Jellyfin Media Server — Home Lab Project
Bryan | Alexandria, VA | May 2026


Overview
This project documents the installation, configuration, and evaluation of Jellyfin, a free, open-source media server deployed on my home Windows server as a direct alternative to Plex Media Server.

The core motivation was to determine whether an open-source solution could match or exceed Plex's feature set without the cost barrier of a Plex Pass subscription ($6.99/mo or a $249 lifetime pass).


Why Jellyfin?
Plex is a polished platform, but many of its most useful features are locked behind a paywall:

Feature
Plex (Free)
Jellyfin
Hardware Transcoding
❌ Plex Pass required
✅ Free
Skip Intro Button
❌ Plex Pass required
✅ Free (plugin)
Custom UI Theming
⚠️ Limited (but default UI is really good)
✅ Full CSS support
Remote Access
⚠️ Relay-limited
✅ Tailscale VPN
Plugin Ecosystem
⚠️ Limited
✅ Active community
Cost
Free (limited features) / $6.99–$249
Completely free


Jellyfin is community-maintained, has no ads, no account requirement, and no paywalled features.


System Environment
Component
Spec
OS
Windows (Home Server)
CPU
AMD Ryzen 5 5500
GPU
Intel ARC B570 (Hardware Transcoding via Intel QSV)
Media Server
Jellyfin (installed via .exe)
Remote Access
Tailscale (Open-Source VPN)
Test Device
iPhone 16 Pro (cellular remote access)



Build Steps
1. Download & Install
Downloaded the Jellyfin Windows installer (.exe) from the official Jellyfin website and ran a standard installation on the home server.
2. Initial Setup
Completed the first-run wizard:

Created an admin account
Enabled remote access in network settings
3. Add Media Library
Added the existing anime library already in use with Plex as the first Jellyfin media source.
4. File & Folder Naming Cleanup
Audited and corrected folder/file names to match Jellyfin's metadata conventions:

Show titles spelled accurately to match database entries
Episode files named consistently (e.g. Show Name S01E01)
5. Custom UI via CSS Theming
Pulled custom CSS themes from the Jellyfin GitHub community and pasted them into Display Settings. Cycled through several options and landed on a theme that significantly improved the default layout.
6. Plugin Installation
Installed two community plugins:

Media Bar Enhanced — richer media player control bar
Intro Skipper — dedicated Skip Intro button per episode (a Plex Pass feature on Plex)
7. Hardware Transcoding — Intel ARC B570 / QSV
Enabled Intel Quick Sync Video (QSV) in Jellyfin's playback settings to offload transcoding from the CPU to the GPU. Still learning and tuning QSV settings for optimal performance.
8. Remote Access via Tailscale
Configured secure remote access using Tailscale (open-source P2P VPN):

Created a Tailscale account
Installed Tailscale on the home server and all mobile devices
Connected to Jellyfin using the server's Tailscale IP
Successfully streamed over cellular on iPhone 16 Pro ✅
9. Ongoing Evaluation
Jellyfin is running in parallel with Plex for active comparison across streaming stability, transcoding performance, and day-to-day usability.


Skills Demonstrated
Windows server software deployment & configuration
Media server setup and library management
Hardware transcoding configuration (Intel ARC / Intel QSV)
Open-source plugin installation and ecosystem navigation
Custom CSS UI theming via community GitHub resources
VPN-based remote access setup (Tailscale)
Cross-platform testing (Windows server, iOS client)
Comparative technology evaluation and documentation


Key Takeaways
Jellyfin delivered on being a fully-featured, cost-free alternative to Plex. Features that require a paid Plex Pass — hardware transcoding, skip intro, advanced UI customization were available for free out of the box or via community plugins.

The main tradeoff is more manual configuration compared to Plex's polished onboarding. For a home lab environment focused on learning and cost efficiency, that's a worthwhile trade.


Next Steps
Continue tuning Intel QSV settings for optimal transcoding performance
Test additional Jellyfin plugins and themes
Monitor long-term stability vs. Plex
Document further configuration changes as the setup evolves



Part of an ongoing home lab portfolio. See also: Plex Media Server, CTDX Threat Detection Project, AI Job Application Automation System.

