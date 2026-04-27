**Nmap (Network Mapper)** is a free and open-source utility used for **network discovery** and **security auditing**. It is widely used by network administrators, security professionals, and ethical hackers to scan networks, identify active hosts, detect open ports, determine running services and their versions, and fingerprint operating systems.

## Basic Nmap Usage
`nmap <scan type> <options> <target>`
**Target Specification:** Can pass hostnames, IP addresses, networks/subnet, etc.
	`-iL` - List of targets from a file.
	`-iR` - Specify number of random hosts.
**Host Discovery:** 
	`-sL` - Lists available targets.
	`-sn` - Disable port scanning. (Ping Scan)
	`-Pn` - Port scan that skips host discovery.
	`-n` - Disable DNS resolution
	`-R` - Resolve IP addresses to hostnames (sometimes default)
![[SCs/Pnscan.png]]
**Basic Scan Types:** 
	`-sS` - Fast stealth scan, default for superusers. (SYN Scan)
	`-sT` - Slow and easily detectable scan, default for non-superusers. (TCP Connect Scan)
	`-sU` - Slowest and most unreliable scan for UDP ports. (UDP Scan)
![[SCs/scantypes.png]]
**Basic Scan Options** 
	`-p` - Port Specification. (eg: `-p22, -p1-100, -p80,443,111,500)
		`--top-ports` - Scans most commonly used ports. Default is 1000.
		`--open` - Show only open or possibly open ports.
	`-sV` - Perform service/version detection.
	`-O` - OS detection.
	`-A` - Enable OS detection, version detection, default script scanning, and traceroute.
![[SCs/ports.png]]
	`-oA` - Saves output in three different formats to a specified file.
	`-v, -vv, -vvv` - Increase output verbosity.
	`-T` - Set timing template. `<0-5>` 5 is the fastest.
	`-sC` - Default script scan.
		`--script=<scriptname>` - Specify which script/s to use.
		![[SCs/script.png]]
	`-f` - Fragment packets making it less likely that they will be detected by a firewall or IDS.
	`-S` - Spoof source IP address. 
	`-g / --source-port` - Specify source port number to use.
	`-D` - Use decoys to perform a scan.
