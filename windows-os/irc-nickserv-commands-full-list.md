# IRC NickServ Commands (full list)

NickServ allows you to “register” a nickname and prevent others from using it. The following commands allow for registration and maintenance of nicknames; to use them, type /msg NickServ command. For more information on a specific command, type /msg NickServ HELP command.

### REGISTER

Syntax: /msg NickServ REGISTER password \[email]Registers your nickname in the NickServ database. Once your nick is registered, you can use the SET and ACCESS commands to configure your nick’s settings as you like them. Make sure you remember the password you use when registering - you’ll need it to make changes to your nick later. (Note that case matters! ANOPE, Anope, and anope are all different passwords!)Guidelines on choosing passwords:Passwords should not be easily guessable. For example, using your real name as a password is a bad idea. Using your nickname as a password is a much worse idea ;) and, in fact, NickServ will not allow it. Also, short passwords are vulnerable to trial-and-error searches, so you should choose a password at least 5 characters long. Finally, the space character cannot be used in passwords.The parameter email is optional and will set the email for your nick immediately. However, it may be required on certain networks. Your privacy is respected; this e-mail won’t be given to any third-party person.This command also creates a new group for your nickname, that will allow you to register other nicks later sharing the same configuration, the same set of memos and the same channel privileges. For more information on this feature, type /msg NickServ HELP GROUP.

### GROUP

Syntax: /msg NickServ GROUP target passwordThis command makes your nickname join the target nickname’s group. password is the password of the target nickname.Joining a group will allow you to share your configuration, memos, and channel privileges with all the nicknames in the group, and much more!A group exists as long as it is useful. This means that even if a nick of the group is dropped, you won’t lose the shared things described above, as long as there is at least one nick remaining in the group.You can use this command even if you have not registered your nick yet. If your nick is already registered, you’ll need to identify yourself before using this command. Type /msg NickServ HELP IDENTIFY for more information. This last may be not possible on your IRC network.It is recommended to use this command with a non-registered nick because it will be registered automati cally when using this command. You may use it with a registered nick (to change your group) only if your network administrators allowed it.You can only be in one group at a time. Group merging is not possible.Note: all the nicknames of a group have the same password.

### IDENTIFY

Syntax: /msg NickServ IDENTIFY passwordTells NickServ that you are really the owner of this nick. Many commands require you to authenticate yourself with this command before you use them. The password should be the same one you sent with the REGISTER command.

### LOGOUT

Syntax: /msg NickServ LOGOUTThis reverses the effect of the IDENTIFY command, i.e. make you not recognized as the real owner of the nick anymore. Note, however, that you won’t be asked to reidentify yourself.

### DROP

Syntax: /msg NickServ DROP \[nickname]Drops your nickname from the NickServ database. A nick that has been dropped is free for anyone to re-register.You may drop a nick within your group by passing it as the nick parameter.In order to use this command, you must first identify with your password (/msg NickServ HELP IDENTIFY for more information).

### ACCESS

Syntax: /msg NickServ ACCESS ADD mask ACCESS DEL mask ACCESS LISTModifies or displays the access list for your nick. This is the list of addresses which will be automatically recognized by NickServ as allowed to use the nick. If you want to use the nick from a different address, you need to send an IDENTIFY command to make NickServ recognize you.Examples:

```
 ACCESS ADD anyone@*.bepeg.com
     Allows access to user anyone from any machine in
     the bepeg.com domain.

 ACCESS DEL anyone@*.bepeg.com
     Reverses the previous command.

 ACCESS LIST
     Displays the current access list.
```

### SET

Syntax: /msg NickServ SET option parametersSets various nickname options. option can be one of:

```
 DISPLAY    Set the display of your group in Services
 PASSWORD   Set your nickname password
 LANGUAGE   Set the language Services will use when
                sending messages to you
 URL        Associate a URL with your nickname
 EMAIL      Associate an E-mail address with your nickname
 ICQ        Associate an ICQ number with your nickname
 GREET      Associate a greet message with your nickname
 KILL       Turn protection on or off
 SECURE     Turn nickname security on or off
 PRIVATE    Prevent your nickname from appearing in a
                /msg NickServ LIST
 HIDE       Hide certain pieces of nickname information
 MSG        Change the communication method of Services
 AUTOOP     Should services op you automatically.
```

In order to use this command, you must first identify with your password (/msg NickServ HELP IDENTIFY for more information).Type /msg NickServ HELP SET option for more information on a specific option.

#### SET DISPLAY

```
 Syntax: /msg NickServ  SET DISPLAY new-display

 Changes the display used to refer to your nickname group in
 Services. The new display MUST be a nick of your group.
```

#### SET PASSWORD

```
 Syntax: /msg NickServ  SET PASSWORD new-password

 Changes the password used to identify you as the nick's
 owner.
```

#### SET LANGUAGE

```
 Syntax: /msg NickServ  SET LANGUAGE number

 Changes the language Services uses when sending messages to
 you (for example, when responding to a command you send).
 number should be chosen from the following list of
 supported languages:
  1) English
  2) Français (French)
  3) Deutsch (German)
  4) Italiano (Italian)
  5) Português (Portuguese)
  6) Español (Spanish)
  7) Türkçe (Turkish)
  8) Catala (Catalan)
  9) ÅëëçíéêÜ (Greek)
 10) Nederlands (Dutch)
 11) Ðóññêèé (Russian)
 12) Magyar (Hungarian)
 13) Polski (Polish)
```

#### SET URL

```
 Syntax: /msg NickServ  SET URL url

 Associates the given URL with your nickname.  This URL
 will be displayed whenever someone requests information
 on your nick with the INFO command.
```

#### SET EMAIL

```
 Syntax: /msg NickServ  SET EMAIL address

 Associates the given E-mail address with your nickname.
 This address will be displayed whenever someone requests
 information on the nickname with the INFO command.
```

#### SET HIDE

```
 Syntax: /msg NickServ  SET HIDE {EMAIL | STATUS | USERMASK | QUIT} {ON | OFF}

 Allows you to prevent certain pieces of information from
 being displayed when someone does a NickServ INFO on your
 nick.  You can hide your E-mail address (EMAIL), last seen
 user@host mask (USERMASK), your services access status
 (STATUS) and  last quit message (QUIT).
 The second parameter specifies whether the information should
 be displayed (OFF) or hidden (ON).
```

#### SET ICQ

```
 Syntax: /msg NickServ  SET ICQ number

 Associates the given ICQ number with your nickname.  This
 number will be displayed whenever someone requests
 information on your nick with the INFO command.
```

#### SET GREET

```
 Syntax: /msg NickServ  SET GREET message

 Makes the given message the greet of your nickname, that
 will be displayed when joining a channel that has GREET
 option enabled, provided that you have the necessary
 access on it.
```

#### SET KILL

```
 Syntax: /msg NickServ  SET KILL {ON | QUICK | IMMED | OFF}

 Turns the automatic protection option for your nick
 on or off.  With protection on, if another user
 tries to take your nick, they will be given one minute to
 change to another nick, after which NickServ will forcibly change
 their nick.

 If you select QUICK, the user will be given only 20 seconds
 to change nicks instead of the usual 60.  If you select
 IMMED, user's nick will be changed immediately without being
 warned first or given a chance to change their nick; please
 do not use this option unless necessary.  Also, your
 network's administrators may have disabled this option.
```

#### SET SECURE

```
 Syntax: /msg NickServ  SET SECURE {ON | OFF}

 Turns NickServ's security features on or off for your
 nick.  With SECURE set, you must enter your password
 before you will be recognized as the owner of the nick,
 regardless of whether your address is on the access
 list.  However, if you are on the access list, NickServ
 will not auto-kill you regardless of the setting of the
 KILL option.
```

#### SET PRIVATE

```
 Syntax: /msg NickServ  SET PRIVATE {ON | OFF}

 Turns NickServ's privacy option on or off for your nick.
 With PRIVATE set, your nickname will not appear in
 nickname lists generated with NickServ's LIST command.
 (However, anyone who knows your nickname can still get
 information on it using the INFO command.)
```

#### SET MSG

```
 Syntax: /msg NickServ  SET MSG {ON | OFF}

 Allows you to choose the way Services are communicating with
 you. With MSG set, Services will use messages, else they'll
 use notices.
```

### UPDATE

Syntax: /msg NickServ UPDATE Updates your current status, i.e. it checks for new memos, sets needed chanmodes (ModeonID) and updates your vhost and your userflags (lastseentime, etc).

### RECOVER

Syntax: /msg NickServ RECOVER nickname \[password]Allows you to recover your nickname if someone else has taken it; this does the same thing that NickServ does automatically if someone tries to use a kill-protected nick.When you give this command, NickServ will bring a fake user online with the same nickname as the user you’re trying to recover your nick from. This causes the IRC servers to disconnect the other user. This fake user will remain online for NickServ to ensure that the other user does not immediately reconnect; after that time, you can reclaim your nick. Alternatively, use the RELEASE command (/msg NickServ HELP RELEASE) to get the nick back sooner.In order to use the RECOVER command for a nick, your current address as shown in /WHOIS must be on that nick’s access list, you must be identified and in the group of that nick, or you must supply the correct password for the nickname.

### RELEASE

Syntax: /msg NickServ RELEASE nickname \[password]Instructs NickServ to remove any hold on your nickname caused by automatic kill protection or use of the RECOVER command. This holds lasts for NickServ; this command gets rid of them sooner.In order to use the RELEASE command for a nick, your current address as shown in /WHOIS must be on that nick’s access list, you must be identified and in the group of that nick, or you must supply the correct password for the nickname.

### GHOST

Syntax: /msg NickServ GHOST nickname \[password]Terminates a “ghost” IRC session using your nick. A “ghost” session is one which is not actually connected, but which the IRC server believes is still online for one reason or another. Typically, this happens if your computer crashes or your Internet or modem connection goes down while you’re on IRC.In order to use the GHOST command for a nick, your current address as shown in /WHOIS must be on that nick’s access list, you must be identified and in the group of that nick, or you must supply the correct password for the nickname.

### INFO

Syntax: /msg NickServ INFO nickname \[ALL]Displays information about the given nickname, such as the nick’s owner, last seen address and time, and nick options. If you are identified for the nick you’re getting information for and ALL is specified, you will be shown all the information; regardless of whether it’s hidden or not.

### LIST

Syntax: /msg NickServ LIST patternLists all registered nicknames which match the given pattern, in nick!user@host format. Nicks with the PRIVATE option set will not be displayed.

### Examples:

```
 LIST *!joeuser@foo.com
     Lists all nicks owned by joeuser@foo.com.

 LIST *Bot*!*@*
     Lists all registered nicks with Bot in their
     names (case insensitive).

 LIST *!*@*.bar.org
     Lists all nicks owned by users in the bar.org
     domain.
```

### ALIST

Syntax: /msg NickServ ALIST \[level]Lists all channels you have access on. Optionally, you can specify a level in XOP or ACCESS format. The resulting list will only include channels where you have the given level of access.Examples: ALIST Founder Lists all channels where you have Founder access.

#### ALIST AOP

```
     Lists all channels where you have AOP
     access or greater.
```

#### ALIST 10

```
     Lists all channels where you have level 10
     access or greater.
```

Channels that have the NOEXPIRE option set will be prefixed by an exclamation mark.

### GLIST

Syntax: /msg NickServ GLISTLists all nicks in your group.

### STATUS

Syntax: /msg NickServ STATUS nickname…Returns whether the user using the given nickname is recognized as the owner of the nickname. The response has this format:

#### nickname status-code

where nickname is the nickname sent with the command, and status-code is one of the following:

```
 0 - no such user online or nickname not registered
 1 - user not recognized as nickname's owner
 2 - user recognized as owner via access list only
 3 - user recognized as owner via password identification
```

Up to sixteen nicknames may be sent with each command; the rest will be ignored. If no nickname is given, your status will be returned.

### SENDPASS

Syntax: /msg NickServ SENDPASS nicknameSend the password of the given nickname to the e-mail address set in the nickname record. This command is really useful to deal with lost passwords.May be limited to IRC operators on certain networks.This command is unavailable because encryption is enabled.
