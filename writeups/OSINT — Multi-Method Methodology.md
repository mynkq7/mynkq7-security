# OSINT — Multi-Method Methodology (Neutral Version)

A structured guide for collecting, analyzing, and using publicly available data for intelligence or investigative purposes.

---

## What is OSINT
OSINT (Open Source Intelligence) refers to gathering and analyzing information from publicly accessible sources.  
The goal is to convert open data into actionable intelligence while maintaining operational security and following legal and ethical standards.

---

## Intelligence Life Cycle

1. **Planning and Direction**  
   Define the objective and scope of the investigation.  
   Establish operational security (OPSEC) protocols, tools, and data sources.

2. **Collection**  
   Gather data from public sources such as websites, social networks, leak databases, and public records.  
   Use both automated tools (SpiderFoot, Maltego) and manual methods (Google Dorks, reverse image search).

3. **Processing and Exploitation**  
   Organize and clean the collected data.  
   Normalize timestamps, locations, and entities.  
   Extract metadata, remove duplicates, and enrich with contextual information.

4. **Analysis and Production**  
   Correlate data to identify patterns, links, and timelines.  
   Validate findings using independent sources.  
   Document analysis clearly with supporting evidence.

5. **Dissemination and Integration**  
   Share verified results with authorized stakeholders.  
   Maintain confidentiality and record chain of custody.

---

## Sock Puppets (Online Personas)

Fake or alternative online identities used to collect data without exposing the investigator’s real identity.

**Key Practices:**
- Maintain full separation between real and fake identities.
- Create a believable history and activity pattern for the account.
- Avoid any digital connection to personal devices or networks.
- Never interact with personal contacts through these accounts.

**Tools:**
- [fakenamegenerator.com](https://fakenamegenerator.com) for identity generation.  
- Burner devices or SIM cards when necessary (ensure legal compliance).  
- Use a VPN or Virtual Machine for all activities.

---

## Search and Dorking Techniques

Use advanced search operators to refine results:

```bash
site:example.com "keyword"
filetype:pdf "name"
inurl:login.php
