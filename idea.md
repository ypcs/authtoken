# Secure authentication token/device
========================================

Just another idea.

## TODO
 - create glossary (host = users pc or other device, token = ...)

## Problems with current devices
 - user needs to trust the PC he/she is using, ie. PC can display 
 falsified information ("You are now paying $9", while in reality user 
 is paying $999)
 - we have no safe way to carry secrets around (private keys especially)
 - often user enters PIN on PC, keyloggers


## Features
 - enough memory to store ALL THE CERTS! (1GB?), MUST be tamper-proof, 
 ie. "if someone opens the device, destroy everything permanently") (and 
 user should have pin code for resetting the device)
 - create/store/export private keys (support disallowing export, and it 
 should be the default)
 - create/store/import/export public keys
 - sign stuff (sign agreements etc.)
 - confirm stuff ("yes, I accept this thing")
  - "yes, I do want to pay $99 to someone@somedomain.com via PayPal"
 - verify stuff
  - "is this really signed by my friend X"
 - encrypt
 - wide support for different types of content
 - two-way authentication (allow verifying user/server)
 - allow pc to use device as certificate store (I can choose my trusted 
 CAs once, and use them with any device)
 - enable pinning certificates
  - pc: "hi, user wants to open somesite.com, somesite.com presents cert 
  XXX, is this ok?", device: "yes/no/unknown"
 - always require physical action to modify content or auth/sign
 - allow multiple identities, never reveal identities to PC (choose 
  current identity on token, not on PC), do not allow PC to identify 
  device (no serial numbers etc.) (PC shouldn't know on which device D 
  my identity I is stored)
 - should work also as HOTP/TOTP token
 - one device should allow multiple users, without revealing one's data 
 to other user
 - software (including all firmware) should be opensource, so user can 
 REALLY trust the device, should be user-flashable
 - carry my WoT with me
 - gpg key signing (attach two devices via cable)
 - all-those-standards, pkcs#11, rsa, shaX, pgp, ...
 - rubberhose encryption <3
 - one device for all eID needs
 - log all actions?


## Hardware
 - screen (display HOTP/TOTP tokens, some signature for the content 
 we're currently processing/accepting/...), black&white is ok
  - we don't trust the host PC, so trusted device should tell us, what 
  we're currently doing
  - display keys as QR code? to export to different device w/o USB 
  connection?
  - "Signing XXX (checksum SHA256 xxxxxxxxxx), are you sure?"
 - numpad (enter pin code, navigate in menus)
 - should be small enough to be carried around, ~always
 - usb/microusb: allow connecting to devices, recharging battery
 - NFC maybe? replace keyfobs that are currently used for opening doors 
 etc. (but: user should be able to turn it off) act as paycard?
 - tamper-proof (clear data if opened etc.)
 - should be crush-safe (shouldn't break if I carry in my pocket)
 - waterproof (oh, this sounds like YubiKey w/ more features now!)
 - should be cheap enough (less than $99)
 - 
