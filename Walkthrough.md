This is an OSINT challenge that requires one to find the flags using information on the open web.

We have been given limited information on the company for this ctf.

<img width="1274" height="446" alt="Screenshot 2025-10-18 111132" src="https://github.com/user-attachments/assets/5f670f8f-e7a7-4777-b058-57db5991150b" />

From the information given, we only have the company name (OSINTOrg) and what we need to find (the flags and the badges).

We have been instructed to find the limited access flag and the full access flag.

## First flag

We can use sherlock to search for the username across multiple sites.

<img width="817" height="232" alt="image" src="https://github.com/user-attachments/assets/fcd87aea-96df-4ee8-a19d-a707422d1790" />

We can head right to the github profile found. We find a profile with 2 employees ,Alex and Emily.

<img width="1835" height="635" alt="image" src="https://github.com/user-attachments/assets/edc50628-223a-405e-a489-91e876d005f5" />

Alex has one repository and no gists but no useful information.
Emily also does not have any useful information on her repository but we do find 2 public gists.
You can access the gists using https://gist.github.com/emilyosintorg

<img width="1823" height="869" alt="image" src="https://github.com/user-attachments/assets/4c682032-3258-40c2-b13e-b80e60025100" />

At the top of the full-badge-disclosure.js file we find a URL.

<img width="1895" height="792" alt="image" src="https://github.com/user-attachments/assets/ff844709-6139-4d4b-be69-89248740bd09" />

When we go to that URL we find some XML code and within it we have a tag labelled key with the name `s3cr3t.txt`.

When we go to https://badge-fullaccess.s3.amazonaws.com/s3cr3t.txt we find the full access flag.

<img width="253" height="75" alt="image" src="https://github.com/user-attachments/assets/3f6b3189-6679-4438-b7b0-aede56b8c44b" />

## Second Flag

When we search for Osintorg on github we get three users with osintorg in their username.

<img width="1063" height="474" alt="image" src="https://github.com/user-attachments/assets/a0874132-259e-4867-82e2-b3c2caab6d16" />

We've already checked out two of them so now we can check out the last user's profile.

The user has one repository which seems to be empty but we can note that it is an update meaning there was a previous version of the file before the update we can see what was changed when we click `update limited badge access`.

Finally we find the final limited access flag.

<img width="916" height="535" alt="image" src="https://github.com/user-attachments/assets/d4cdf402-d36c-4984-85b4-b2c9f55de728" />

With that we have completed the Badge hacking OSINT CTF by vulnmachines.

## Congratulations and happy hacking, ethically of course
