# ThetaKVM
KeyVault Manager
For those who just want to run the app, download the file: ThetaKVM_Win64_Release.zip 

## Inspiration
Parents, friends, loved ones and all those who have come to me late at night on Discord telling me they lost all their crypto and asking for help due to one reason or another.

As the world embraces crypto, we should seriously start considering how we store access to our greatest investment of all time.  Ask yourself, "do I trust my most valuable assets in the hands of a third party?" 

I'd like to think programs like MetaMask and LastPass are safe, and for the most part, they are... until one rogue employee pushes out a single line of code update that scrapes all keyboard inputs for 24 hours until it's flagged and removed, however by then it's too late.  Most commercial wallets have full visibility into your private-key and other sensitive data pertaining to your wallets the moment you type in your password, provide nothing more than a false sense of security... consider especially an extension which might be completely safe, however it is operating on a zero-day vulnerable web-browser (and even Brave is Chrome based).

## What it does
KVM (originally called "WalletManager" when I started writing it) is something I've wanted to write for a minute now.  Recently a good friend and I embarked on a little venture which required sharing a wallet; sending the keystore, mnemonic, or any other portion of the wallet over any digital medium (txt, email, Teams, etc...) just didn't seem safe and also keeping track of the info (you'd be surprised how easy it is to have 10+ different wallets, as a developer with ADHD I can attest, keeping track of them all can be a nightmare).  This program allows you to organize your wallets in one file (called a "KeyVault"), organized in folders (individually referred to as a "KeyBase"), while "safely" storing and secure your keystores along with any other relative sensitive information (via a second-level password).  Note, I put quotes around "safely" as with anything, all things are hackable and milage may vary.  For this app I wanted to use all MS2019 native functionality, therefore data is encrypted using TripleDES and a salted MD5 for hashing, which in short means set a long password (at least 11 characters long) for your VaultCrypt password as the data is encrypted w/the passwords supplied.  Future versions will support AES-256 for encryption and BCRYPT for hashing.

## How it was built it
- VisualStudio 2019 VB.NET (yes, VB, I only had 10 days to write this app).  
- All libraries are native to VS2019.

## Challenges run into
Microsoft.
- Wanting to develop something really kick butt, however not wanting to import external 3rd party  libraries (i.e. BCRYPT, BLOWFISH, etc...)

## What I learned
- Don't save a (full) hash locally unless you want it hacked.
- How easy it is to add salt.

## What's next for ThetaKVM!
- Linux and Mac version
- User/Group management (with dynamic salt)
- Permission defined KeyBase Export/Import functionality for simplified sharing.
- Add encryption support for AES-256 & BCRYPT
- Additional 3rd party support and branded (with permission) logos
- Future Forks in the works:
 - "Online Edition" which makes calls made directly to Theta's API
 - "Wallet Edition" which runs on a Guardian Node (aka a true Theta Wallet), does not require to be staked to however the node will act as a fully independent Wallet GUI that doesn't need to speak with the Internet (it does however need to speak w/the locally running GN).



