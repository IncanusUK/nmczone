# Namecoin To Zonefile

This script generates a BIND zonefile from the Namecoin blockchain.

### Requirements
- Running instance of Namecoin
- jsonrpclib - `pip install jsonrpclib`

### Instructions
1. Clone this repository into `/opt/nmczone/` or a path of your choice
2. Install and configure Namecoin in `~/.namecoin/namecoin.conf`
3. Install and configure BIND
4. Populate `nmczone.conf` with the user and password from `~/.namecoin/namecoin.conf`
5. Add the authoritative nameserver and contact email in `nmczone.conf`
6. Run the script `update.sh` via cron at an interval of your choice.

### Supported Records

From [Namecoin Domain Name Specification 2.0](http://wiki.namecoin.info/?title=Domain_Name_Specification_2.0)

| Type      | Corresponding DNS Record  |
|:---------:|:-------------------------:|
| ip 		| A							|
| ip6 		| AAAA						|
| alias 	| CNAME						|
| translate	| DNAME						|
| ns		| NS						|
| map		| 							|

### To Do

| Type      | Corresponding DNS Record  |
|:---------:|:-------------------------:|
| service 	| SRV						|
| delegate	| 							|
| import	| 							|
| ds		| DS						|
| loc 		| LOC						|
