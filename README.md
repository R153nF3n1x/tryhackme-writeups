# TryHackMe Write-Ups

A collection of hands-on CTF and lab write-ups from TryHackMe, covering SOC analysis, OSINT, phishing investigation, DFIR, AI security, web exploitation, network forensics, and cloud security.

**TryHackMe:** [RisenFenix](https://tryhackme.com/p/RisenFenix)

---

## Folders

| Folder | Description |
|--------|-------------|
| [SOC Level 1 Learning Path](./SOC%20Level%201%20Learning%20Path) | Phishing analysis, OSINT, SIEM, network forensics, and web vulnerability fundamentals |
| [AI Security Learning Path](./AI%20Security%20Learning%20Path) | Prompt injection, RAG exposure, ML supply chain attacks, LLM threat modelling, OT/ICS |
| [Hacker Holidays](./Hacker%20Holidays) | Progressive resort-themed CTF covering web exploitation, cloud, PCAP, RE, and boot2root |
| [Love at First Breach](./Love%20at%20First%20Beach) | Valentine's Day CTF covering JWT attacks, XSS, file upload RCE, IDOR, and MD5 collision |

Standalone write-ups not assigned to a folder are listed directly in this repository.

---

## AI Prompt for Write-Up Generation

When starting a new write-up session in Claude, paste the following prompt first to get consistently formatted output:

```
You are a TryHackMe CTF write-up assistant. When I provide room details, generate a clean GitHub markdown write-up in exactly this format with no dash dividers between sections:

# Room Name - TryHackMe: [name]
Date: DD Month YYYY
Difficulty: Easy / Medium / Hard
Category: [category]

# Scenario
# Tools Used
# What I Did
# What I Found
# Key Learning
# What I Would Flag in a Real SOC

Rules:
- No horizontal dividers between sections
- No bold text inside bullet points
- No em dashes
- Sentence case throughout
- What I Found as bullet points only, no tables
- Keep it concise but professional
- Include commands in code blocks where relevant
```
