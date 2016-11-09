# KeyConv (vanitygen) #
---
This is keyconv utility from [samr7/vanitygen](https://github.com/samr7/vanitygen) repository with added **-X** key - Generate address with the given version option.

My mate @kolobus sometimes ago told me about [Komodo Platform](https://komodoplatform.com/), i'm first time hear about vanity addresses and other things and was interested in this. However, I have found that keyconv utility doesn't support generation any type of addresses except BitCoin. This "fork" fix this. For example if we need to gen some Komodo addresses:

    keyconv -X 60 -G

Result is:

    Pubkey (hex): 04abc6977702a250a2153888b3a65f61153aeb9980ba16df85ac57b12046ac8839a44a2a1dd389c55cc9dfe3d3fb56f2a5203efd2973a4dcbbf8004b23257a828e
    Privkey (hex): E5EBF2F9886401C147F18F38D98AB401592243BAB284A8DEFA27660E3DC67C80
    Address: RMKzCMRCMwt41CkSZc8aJ7wWHe1ZSA9dPS
    Privkey: 7LCDCx4rJu4W44YB9rACd26S1GYcQ3WwVPFDwH8zWex96zBBipc

If we want to get Pubkey from Privkey:

    keyconv.exe -v -X 60 7LCDCx4rJu4W44YB9rACd26S1GYcQ3WwVPFDwH8zWex96zBBipc

And result is the same:

    Pubkey (hex): 04abc6977702a250a2153888b3a65f61153aeb9980ba16df85ac57b12046ac8839a44a2a1dd389c55cc9dfe3d3fb56f2a5203efd2973a4dcbbf8004b23257a828e
    Privkey (hex): E5EBF2F9886401C147F18F38D98AB401592243BAB284A8DEFA27660E3DC67C80
    Address: RMKzCMRCMwt41CkSZc8aJ7wWHe1ZSA9dPS
    Privkey: 7LCDCx4rJu4W44YB9rACd26S1GYcQ3WwVPFDwH8zWex96zBBipc

Also, since i use Windows based OS i make compile.cmd batch file to easy build project under MSVC. Win32 binary is inlcluded. For all who wants build it under other OS, clone the original repository from [here](https://github.com/samr7/vanitygen), change the keyconv.c on modified from this git and build.

For successful build under Windows you should put all needed dependencies in external folder:

- openssl
- pcre-win32
- pthreads-w32-2-9-1-release

## Credits ##

- [samr7/vanitygen](https://github.com/samr7/vanitygen) - original sources.
- BitCoin Donate: 1DeckerNWuk9s4MnCvtxCEh4osCgNotH9w
- Komodo/BTCD Donate: RDecker69MM5dhDBosUXPNTzfoGqxPQqHu

