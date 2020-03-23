# Dsturb
Network Traffic Controller

Supported OS (Linux, Darwin, Free-BSD)

### Installation
Clone this repo using git clone
```
git clone https://github.com/avivbintangaringga/dsturb.git
```
Then go to the package directory and install
```
make install
```
### Getting Started
Helper contents
    
	Options:
            -c  --connect                     Enable internet access on target
            -d  --disconnect                  Disable internet access on target
            -r  --randomize                   Randomize interface's MAC Address
            -e  --exclude   [IP,IP,IP,...]    Exclude the following IP Addresses
            -L  --limit     [rate-limit]      Limit bandwith for target
            -h  --help                        Display help
    
         Supported rate limit units:
             b   ->  bits per second
             k   ->  kilobits per second
             m   ->  megabits per second
             g   ->  gigabits per second
             t   ->  terabits per second
             B   ->  Bytes per second
             K   ->  Kilobytes per second
             M   ->  Megabytes per second
             G   ->  Gigabytes per second
             T   ->  Terabytes per second
             (default: b)
    
             e.g: 10K, 500K, 1M, 10M
### Example:
Forward target internet access and keep current MAC Address
```
sudo dsturb -c wlp3s0
```
Limit target bandwith with excluded address
```
sudo dsturb -cL 50K -e "network_id.host_id1 network_id.host_id2" wlp3s0
```
Drop target internet access and randomize current MAC Address
```
sudo dsturb -dr wlp3s0
```
### Authors
[Aviv Bintang Aringga](https://github.com/avivbintangaringga)

[Syahid Nurrohim](https://github.com/syahidnurrohim)

