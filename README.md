# d_tools
the tool for external recon

# process
1. passive recon
   1.1 collect subdomains (crt, wayback)
   1.2 resolve subdomains -> get IP
   1.3 resolve IP -> check if any new TLD
   1.4 get full extended list of TLD

2. for each TLD
   2.1 get subdomains
   2.2 get IPs
   2.3 ports and services
   2.4 URLs and JS urls

# CHANGE LOG
* move configs into folder
* make 'words' folder  - update Docker to copy dics there + some crafted
* IP clean from 1.1.1.1
* make Tech summary
* tlsx_san - make enhanced list of TLDs - re-run subdomains?
* make scope control script
* make whois readable summary
* check ping
* make ping readable summary -> new TLDs
* API analysis - after JS: subdomains final subdomain + gospider: cat subdomainizer_scan.txt | python3 /scripts/checkiner.py /localshara/scope_seeds.txt | sed 's|^|https://|' | httpx
* make analysis of gospider linkfinder? do we need separate command?
* Docker - copy of wordlists
* Docker - install cvemap
* Docker - nmapsilent script - make binary
* make chown  - see internal script
   
   
