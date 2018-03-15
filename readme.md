# Description
* Woody CPU miner implemented in C++
	* based on a modified version of phc-winner-argon2, libcurl, libopenssl and gmp / mpir
	* can be a little bit faster than java miner (up to 4% faster on Windows10)
	* dev fee: first share, then 0.5% of next shares found (1 on 200, randomly)
	* only pool mining for now (no solo mining)
* There are 3 versions, slowest to fastest:
	* woodyminer: for older cpu not supporting AVX
	* woodyminer_avx: for cpu supporting AVX
	* woodyminer_avx2: for recent cpu supporting AVX2

# Download Binaries
* Up to date binaries can be found here:
	* https://bitbucket.org/cryptogone/woodyminer/downloads/

# Installation / Basic usage
* Windows:
	* unzip the archive to a folder
	* launch one of woodyminer / woodyminer_avx / woodyminer_avx2
* Linux:
	* IMPORTANT: first install required packages by running: 
		* sudo apt-get install libssl-dev libcurl3
	* unzip the archive to a folder
	* open a terminal
	* use 'cd' command to go into the folder
	* launch ./woodyminer or ./woodyminer_avx or ./woodyminer_avx2 depending on what your cpu supports
* Mac:
	* unzip the archive to a folder
	* launch one of woodyminer / woodyminer_avx / woodyminer_avx2
* On first launch the miner will ask you to enter some informations (ex: your wallet address) in order to create a config file (config.cfg)
* If you want to restart the config process, just delete config.cfg and restart the miner
* The config file uses the same format as java miner, so you can reuse the one you have from it
 
# Advanced usage
* Tou can pass commandline parameters to the miner, for example (linux/mac terminal):
	* ./arioCppMiner -a wallet_address -p pool_url
* To see all available parameters: 
	* ./arioCppMiner -h
* IMPORTANT:
	* CLI parameters override the values from configuration file
	* if you pass any CLI parameter the first time you launch the miner, it will skip the configuration step (useful for scripted install on a server/VM)

# Building
* git hub repo:
	* https://github.com/petesweeps/woody
 * Clone the repository then see instructions in build_win.md / build_linux.md / build_mac.md

# Compatibility
* Windows10 64bits
* Linux 64bits: tested on Ubuntu 16, Xubuntu 17 and Ubuntu 16 server
* MacOs: tested on MacOS 10.13 (High Sierra)
* You can use a tool like CPUZ to check if your system supports AVX / AVX2 and chose the correct exe
* 32bits platforms not supported

# Contact / Reporting bugs
* Email: woody.dev@gmail.com
* Discord: woodminer#1968
* Report bugs: https://github.com/petesweeps/woody
