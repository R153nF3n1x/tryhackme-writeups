#Room Name - TryHackMe Neighbour
**Date: 16 March 2026**
**Difficlty: Easy**
**Category: IDOR**

#Scenario
Check out our new cloud service, Authentication Anywhere. Can you find other user's secrets?
The challenge was based on IDOR concept.

#Tools Used
- TryHackMe Attack Box
- Browser

#What I Did
- Navigated to the provided IP address using the TryHackMe attack box.
- Tried logging in using the username/password as admin, and few other commonly used one, did not work.
- Checked the source code and noticed that we can access the guest:guest account. Logged in with the same.
- Noticed that the enpoint is profile.php?user=guest, tried with user=admin, was able to access and retrieved the flag.

#What I Found
flag{66be95c478473d91a5358f2440c7af1f}

#Key Learning
Source code can expose valid credentials or reveal parameter structures that indicate IDOR vulnerabilities, always review page source before attempting authentication bypass.

#What I would Flag in a Real Soc
- Ensure all user-specific endpoints validate that the authenticated session matches the requested resource
- Implement server-side authorisation checks — never trust client-supplied user identifiers alone
- Include IDOR testing in pre-launch security reviews and penetration testing scope 
