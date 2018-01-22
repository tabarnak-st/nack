How to install:

This for required old linux distribution package since we try upgrade new

Debian Jessie & Os used GCC4.x ver

- open terminal and try 

apt update && apt upgrade

- try copy and paste this

apt install build-essential libqt4-dev qt5-qmake cmake qttools5-dev libqt5webkit5-dev qttools5-dev-tools qt5-default python-sphinx texlive-latex-base inotify-tools  openssl libssl-dev libdb++-dev libminiupnpc-dev git sqlite3 libsqlite3-dev g++ libpng-dev git g++ gedit python gcc-4.9 g++-4.9 make libbz2-dev libdb++-dev libdb-dev libssl-dev openssl libreadline-dev autoconf libtool git libleveldb-dev libblkid-dev e2fslibs-dev libboost-all-dev libaudit-dev

- try clone it used this

git clone https://github.com/FndNur1Labs/DirhamCli.git && git status

- [alternative dev:who expert in c++]try do

git checkout -b develop && git pull origin develop

- then build

cd DirhamCli && make

Debian Strech && Ubuntu 16.x

- Still Developing

Mac

- Need instructor

Premine Enable :

- Edit src/daemon/daemon.cpp

//const command_line::arg_descriptor<std::vector<std::string>> arg_genesis_block_reward_address = {"genesis-block-reward-address", ""};
 } 

go to

//premine daemon
[function]

and search //command_line::add_arg(desc_cmd_sett, arg_genesis_block_reward_address);

- Edit src/cryptonotecore/currency.cpp

//genesisBlockReward(parameters::GENESIS_BLOCK_REWARD);

//premine
[function]

- Edit src/cryptonotecore/currency.h

//uint64_t genesisBlockReward() const { return m_genesisBlockReward; }

//premine
[function]

- Edit src/Rpc/CoreRpcServerCommandsDefinitions.h

//premine
[function]

seach this

 //premine
  //  CurrencyBuilder& genesisBlockReward(uint64_t val) { m_currency.m_genesisBlockReward = val; return *this; }

you can remove "//"

ICO & POS Enable :

- Edit src/cryptonoteconfig.h

//coin ico
const uint64_t POINT                                         = UINT64_C(1000);        // pow(10, 3)

-----

//premine
const uint64_t COIN                                           = UINT64_C(1000000);     // pow(10, 6)

-----

//ico & pos
const uint64_t START_BLOCK_REWARD                            = (UINT64_C(100) * parameters::POINT);
const uint64_t ICO_BLOCK_REWARD	                             = (UINT64_C(18446744073) * parameters::COIN); // 18.4 billion ICO
const uint64_t MAX_BLOCK_REWARD                              = (UINT64_C(10) * parameters::COIN);
const uint64_t REWARD_INCREASE_INTERVAL = (UINT64_C(264000));

- Edit src/cryptonotecore/currency.cpp

//ico & pos
[function]

you can remove "//"

For Become Collabolator can PM us!or just git push on develop. we will review your codes
