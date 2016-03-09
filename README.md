##  Raspi Ethereum Node
A raspberry pi with Rasbian OS makes the perfect development network for Ethereum! Extra bonus if the raspi has a wifi connection and you can SSH into it using putty or a terminal.  

1. Download the precompiled binary from master branch
>wget https://build.ethdev.com/builds/ARM%20Go%20master%20branch/geth-ARM-latest.tar.bz2

2. Unpack the compressed file
>tar -xjvf geth-ARM-latest.tar.bz2

3. Copy it to a location in $PATH (i.e. /usr/bin/local) as an administrator
> sudo cp geth /usr/bin/geth

4. Increase permissions for geth so port binding works
> sudo chmod a+x /usr/bin/geth

5. Generate an account
> geth account new

6. Start mining
> geth --etherbase "0" --rpc --rpcaddr "127.0.0.1" --rpcport "8545" --dev --mine

Now you can make RPC calls to the raspberry pi as if it were an Ethereum testnet.  New coins will be minted into the etherbase account.
