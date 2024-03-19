<p align="center">
  <img width="100" src="https://imgur.com/3cw4DQr.png" alt="NetScan Security Logo" />
  <h2 align="center">NetScan ANTI-Virus</h2>
  <p align="center">Precision Scans, Real-time Defense</p>
</p>

# Description
A Windows antivirus written in VC++.

## Overview of Working

Fundamentally an antivirus is a program that scans for malicious files in the machine and tries to detect, stop (if the virus is in effect), quarantine the virus inside a vault (by tweaking it and deactivating it), and  when required deleting it.

The Application we have created above is a static antivirus that scans a given directory for malicious files by,
1. Reading the internals of the file if it is a batch program or if it contains any harmful commands.
2. Comparing the  hash of the file being scanned with the hash of well-known viruses of which we maintain a database. (The thing that gets updated when you update an antivirus, So it is a continuous process).

As it is just a fun project we chose to use md5 hash which is not collision resistant (There are collision demos available), hence not to be used for serious projects. SHA256 and SHA512 can be used for such projects.
The hash database used in our application is very small and just for demonstration purposes only, which you can update by using the Update Database option and manually adding a virus hash by giving it a virus file or finding the hash of a malicious program online and copying it in “hashes.txt” with each new hash on newline.

A dynamic antivirus (nowadays most antivirus try to do so but none is 100% successful yet, for it would require a successful AI program to do so, which is ideal) would scan the running processes inside the main memory of the machine which might be harmful by detecting their execution behavior at runtime.


## Interacting with the Antivirus

**Quick Scan:** Compare the hashes of files being scanned with the hash database.

**Deep Scan:** Reading files for malicious code (which can be edited in “db.txt”).

**Fix Shortcut:** Removes the annoying Flash drive shortcut virus.

**Virus Vault:** The viruses found are moved to the vault and using it you can delete those viruses.

**Update Database:** Update the antivirus database.

Other screenshots of the Antivirus are available in the Images folder of this repository.
