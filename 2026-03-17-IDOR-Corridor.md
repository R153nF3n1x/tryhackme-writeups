#Room Name - TryHackMe Corridor
Date: 16 March 2026
Difficulty: Easy
Category: IDOR / Hash Manipulation

#Scenario
Can you escape the Corridor? The challenge revolves around identifying hidden values behind hashed URLs and exploiting predictable patterns.

#Tools Used
TryHackMe Attack Box
Browser
Online Hash Analyzer / Generator

#What I Did

Navigated to the challenge using the TryHackMe Attack Box.

Hovered over each corridor and observed that each link contained a hash value.

Collected all hash values and analyzed them using an online hash analyzer.

Identified that the hashes were MD5 hashes mapped to numeric values.

Discovered mappings:

1679091c5a880faf6fb5e6087eb1b2dc → 6

8f14e45fceea167a5a36dedd4bea2543 → 7

a87ff679a2f3e71d9181a67b7542122c → 4

c4ca4238a0b923820dcc509a6f75849b → 1

c81e728d9d4c2f636f067f89cc14862c → 2

eccbc87e4b5ce2fe28308fd9f2a7baf3 → 3

e4da3b7fbbce2345d7772b0674a318d5 → 5

6512bd43d9caa6e02c990b0a82652dca → 11

c20ad4d76fe97759aa27a0c99bff6710 → 12

c51ce410c124a10e0db5e4b97fc2af39 → 13

d3d9446802a44259755d38e6d163e820 → 10

Noticed that values 8 and 9 were missing from the sequence.

Generated MD5 hashes for 8 and 9, but both led to empty rooms.

Then tested edge cases and tried the value 0.

Generated MD5 hash for 0:

0 → cfcd208495d565ef66e7dff9f98764da

Accessing this hash revealed the flag.

#What I Found
flag{2477ef02448ad9156661ac40a6b8862e}

#Key Learning
Predictable hashing patterns (like MD5 of sequential integers) can be exploited to enumerate hidden resources. Missing values in sequences often indicate potential entry points, and testing edge cases such as 0 or negative values can reveal unintended access paths.
