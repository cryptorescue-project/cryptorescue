<p align="center">
  <img src="https://raw.githubusercontent.com/cryptorescue-project/CryptoRescue/master/doc/cryptorescue.png">
</p>


CryptoRescue Website
=====================================

https://cryptorescue.org

What is CryptoRescue?
----------------

Here at CryptoRescue, we are driven by a single goal; to do our part in making the world a better place for all animals. We strive to build productive relationships and make a positive impact with all organizations big and small to assist with donations. With this initiative, our goal is to promote great opportunities for those in need with the rescued animals. Learn more about our work by getting in touch with our team today.

For more information, as well as an immediately useable, binary version of
the CryptoRescue software, see https://cryptorescue.org

# Build on Ubuntu 16.04
-------
## Dependencies:
 
sudo apt-get install git
 
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
 
sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
 
sudo apt-get install libboost-all-dev
 
sudo apt-get install software-properties-common
 
sudo add-apt-repository ppa:bitcoin/bitcoin
 
sudo apt-get update
 
sudo apt-get install libdb4.8-dev libdb4.8++-dev
 
sudo apt-get install libminiupnpc-dev
 
sudo apt-get install libzmq3-dev
 
sudo apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler
 
sudo apt-get install libqt4-dev libprotobuf-dev protobuf-compiler

## Build Process:

git clone https://github.com/cryptorescue-project/cryptorescue.git

cd cryptorescue

./autogen.sh

./configure --enable-cxx --disable-shared --with-pic --prefix=$BDB_PREFIX CXXFLAGS="-fPIC" CPPFLAGS="-fPIC"

make

License
-------

CryptoRescue is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/cryptorescue-project/CryptoRescue/tags) are created
regularly to indicate new official, stable release versions of CryptoRescue.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://lists.linuxfoundation.org/mailman/listinfo/cryptorescue-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #cryptorescue-project-dev.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

Testnet is now up and running and available to use during development. There is an issue when connecting to the testnet that requires the use of the -maxtipage parameter in order to connect to the test network initially. After the initial launch the -maxtipage parameter is not required.

Use this command to initially start cryptorescued on the testnet. <code>./cryptorescued -testnet -maxtipage=259200</code>

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`


### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.


About CryptoRescue
----------------
A digital peer-to-peer network for the facilitation of asset transfer. Optimzed for miners who have encountered power management issues (power fluctuation volatility) in their experiences thus far with the new x16r mining algorithm. 

Thanks and due credit are extended to the Bitcoin and Ravencoin developers, as well as Pigeoncoin. 

The CryptoRescue project is launched based on the hard work and continuous effort of over 400 Bitcoin developers who made over 14,000 commits over the life to date of the Bitcoin project, as well as those developers who worked on Ravencoin and Pigeoncoin, the reference implementation of x16r and x16s. We are eternally grateful  for their efforts and diligence in making secure networks, and their support of free and open source software development. The CryptoRescue experiment rests solidly on the foundation you built.

Our Mission
Here at CryptoRescue, we are driven by a single goal; to do our part in making the world a better place for all animals. We strive to build productive relationships and make a positive impact with all organizations big and small to assist with donations. With this initiative, our goal is to promote great opportunities for those in need with the rescued animals. Learn more about our work by getting in touch with our team today.

Abstract
CryptoRescue aims to implement a blockchain which is optimized specifically for the use case of transferring assets such as securities from one holder to another. Based on the extensive development and testing of Bitcoin, CryptoRescue is built on a fork of the Bitcoin code. Key changes include a faster block reward time and a change in the quantity of coins. Note that the coin quantity change does not change the inherent weighed distribution schedule.

CryptoRescue is free and open source and will be issued and mined transparently with no pre-mine, developer allocation or any other similar set aside. CryptoRescue is intended to prioritize user control, privacy and censorship resistance and be jurisdiction agnostic while allowing simple optional additional features for users based on need.


High Level Background
A blockchain is a ledger showing all transactions made with a curerncy, including a coin or transaction's value - as well as the ability to for currency to be transferred to other parties. Of all the possible uses for blockchains, the reporting of who owns what is one of the core uses of the technology.  This is why Bitcoin was first and most successful use case for blockchain technology to date.

The success of the Etherium ERC 20 token shows the demand for tokenized assets that use another blockchain.  Tokens offer many advantages to traditional shares or other participation mechanisms such as faster transfer, possibly increased user control and censorship resistance and reduction or elimination of the need for trusted third parties.

Bitcoin also has the capability of serving as the rails for tokens by using projects such as Omnilayer, RSK or Counterparty. However, neither Bitcoin nor Ethereum was specifically designed for facilitating ownership of other assets. 

CryptoRescue is designed to be a use case specific blockchain designed to efficiently handle one specific function: the transfer of assets from one party to another.

Bitcoin is and always should be focused on its goals of being a better form of money. Bitcoin developers will unlikely prioritize improvements or features which are specifically beneficial to the facilitation of token transfers.  One goal of the CryptoRescue project is to see if a use case specific blockchain and development effort can create code which can either improve existing structures like Bitcoin or provide advantages for specific use cases.

In the new global economy, borders and jurisdictions will be less relevant as more assets are tradable and trade across borders is increasingly frictionless. In an age where people can move significant amounts of wealth instantly using Bitcoin, global consumers will likely demand the same efficiency for their securities and similar asset holdings.

For such a global system to work it will need to be independent of regulatory jurisdictions.  This is not due to ideological belief but practicality: if the rails for blockchain asset transfer are not censorship resistance and jurisdiction agnostic, any given jurisdiction may be in conflict with another.  In legacy systems, wealth was generally confined in the jurisdiction of the holder and therefor easy to control based on the policies of that jurisdiction. Because of the global nature of blockchain technology any protocol level ability to control wealth would potentially place jurisdictions in conflict and will not be able to operate fairly.  

