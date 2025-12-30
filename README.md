# d_tools
the tool for external recon

# process
1. quick passive recon \
   1.1 collect subdomains (crt, wayback) \
   1.2 resolve subdomains -> get IP \
   1.3 resolve IP -> check if any new TLD \
   1.4 get full extended list of TLD

2. for each TLD \
   3.1 get subdomains \
   3.2 get IPs \
   3.3 ports and services \
   3.4 URLs and JS urls \

Module 1: general commands
input: seed_domains.txt
process: check ping, check whois history hacktrails, check whois
output: TLD_domains_OK.txt

Module 2: subdomains
input: domain
process: amass, subfinder, crt.sh etc - passive
output: subdomains_clean, subdomains_cool

Module 3: IP
input: subdomains_clean
process: dnsx, ipinfo
output: ip.txt, ip_info.txt, domains_ip.txt 

Module 4: ports and services
input: IP.txt
process: shodan smap
output: ports open // need to be added into one json object... for all subdomains

Module 5: tls and additional domains
input: IP.txt
process: tlsx
output: get the list of addiitonal domains from the same IP // need analysis of neihbors, filtering for 1.1.1.1

Module 6: photon
input: subdomains_clean
process: photon
output: URLs


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
* make chown  - see internal script

# docker log
* Docker - copy of wordlists
* Docker - install cvemap
* Docker - nmapsilent script - make binary
* Docker - python: add requests
   
   
