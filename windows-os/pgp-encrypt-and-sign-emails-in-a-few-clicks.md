# PGP: Encrypt & sign emails in a few clicks

Nowadays it is increasingly necessary to protect your data, so we have added support for PGP technology in eM Client version 7.2. PGP stands for Pretty Good Privacy. With PGP, you can digitally sign and encrypt emails without having to register with a certification authority.

## PGP

### Why use email digital signatures in electronic mail

Digital signatures give your email recipients assurance that the messages received were sent from the proper sender and not tampered with. You can equally check the senders’ identity of signed received emails and be sure there were no changes made on the road. Email digital signatures verify the communication parties’ identity, but do NOT make the emails encrypted as such.

### Why and when to use email encryption

Whenever you want to be sure no one without access to your personal key (and the password to it) reads your messages, including on your own computer, use encryption. This applies to mailbox providers as well, as the encrypted message is secured during its entire journey.

### What does PGP stand for

PGP is acronymous to “Pretty Good Privacy” and was invented already in 1991. Despite being connected mainly to email communication, PGP can be applied to any texts or files.If you are further interested, read a more detailed explanation of PGP at the end of this article.

### Alternatives to PGP

Obviously, PGP is not the only technology to use for email encryption and signatures. eM Client also supports the S/MIME standard, which works on a similar two-key principle, but requires a Certificate Authority for verification, which can make the process of secure communication more expensive and clumsy.

### How to use PGP in eM Client

You might ask ‘How to encrypt my message?’ To start using PGP in eM Client, you need to create or import the public and private key for each email address you want to encrypt/sign messages with. This can be done in Menu > Tools > Settings > Signing and Encryption > Certificates and Keys.

### PGP Setup

Those who never used PGP before can generate their new keypairs by clicking the “Create PGP certificate” button. Choose an email address to assign the keypair to, input name, password, and click “OK” – this will create your new set of keys.If you have your PGP keys already generated, just import them via the “Add certificate/key” button.

### Key distribution

When you are set up, you will want to distribute your Public key to people you plan to exchange secured messages with.The easiest way to do this is to double-click onto an email encryption certificate in “My certificates/keys” section in order to open the certificate detail, and click the “Send” button to distribute your keys to recipients of your choice. The recipients will get a message with an attached key, which they can easily import into the eM Client PGP key storage.It is important to verify such a key with recipients also via other communication channels than just email – e.g. via phone. You simply call each other and compare the Fingerprint code of incoming and outgoing keys (which you can find in the key details).

### Sending encrypted emails

After having exchanged PGP keys with your contacts, you can proceed with sending signed and/or encrypted emails. Icons for email encryption (a lock) and digital signature (a stamp) should appear in the new message editor toolbar in eM Client.

Once you decide to send an encrypted message, eM Client will automatically select the proper encryption technology to apply – S/MIME or PGP – based on the recipients’ public certificates and keys.

If there are no valid public keys available for selected recipients, a warning notification appears before the message is actually sent out.

The first detected key is used for your email digital signature, but it is possible to select a key manually, should you use more keys for the same email address.

#### Different PGP formats for encryption

When using the PGP technology, you can decide for PGP/MIME or Inline PGP format.

eM Client automatically selects the most suitable option, in most cases PGP/MIME that allows encryption of text formatting as well as attachments.

In comparison, Inline PGP is a simpler format that only encrypts plain text and is a preferred choice if you wish to maximize compatibility with other applications.

The automatic selection of PGP format settings can be changed in Menu > Message > Format of PGP.

#### Reading of encrypted/signed messages

To open and read a signed and/or encrypted message is very simple in eM Client. The email digital signature gets automatically validated upon opening the email. To enable the signature validation, you need to have the sender’s public key saved in eM Client or in the operating system. As long as the signature is valid, ergo the message was not tampered with, a notification with “This message was signed” would appear under the message header.

In order to read a message with encryption, eM Client requires your private password-protected PGP key. After entering the password, the message gets decrypted and you are free to read its content.

#### PGP in a nutshell

The main concept used by PGP (as well as S/MIME) is public-key cryptography, also known as asymmetric cryptography.

In this encryption system, every user obtains two keys that are connected through user’s email address:

A private key that should be kept secret and not revealed to anybody. It’s used to digitally sign outgoing messages, or to decrypt incoming messages.

A public key that is to be distributed to other users. Public key is used to validate the digital signature of incoming messages, or to send encrypted messages to other users.

This differentiation of keys makes the very foundation of message encryption and signing.

Each PGP key features a unique Fingerprint consisting of a short string of numbers and letters. This feature allows users to easily verify keys sent via unsecured channels – such as email itself – and to be sure the keys were not altered on the road, which would threaten their future communication safety.

The fingerprints on sender’s and recipient’s side should be compared via a third channel, e.g. a phonecall.

There are two ways to use PGP in emails:

PGP/MIME, a PGP standard that allows encryption and signature of the entire message, including formatted text and inserted pictures or attachments, or Inline PGP, a simpler standard that encrypts plain text only, with no attachments.

In order to maximize compatibility, eM Client supports both PGP standards for sending and receiving messages.

Our ultimate goal is to grant you with means of secure communication in the new era of digital threats. Now you have all the information and tools needed to ultimately protect your emails.
