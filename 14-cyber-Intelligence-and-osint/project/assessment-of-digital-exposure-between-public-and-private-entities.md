# Assessment of Digital Exposure between Public and Private Entities

This project aims to apply OSINT (Open Source Intelligence) techniques to compare the **digital exposure surface** of two real organizations: one from the public sector and one from the private sector. Your goal is to analyze, document, and compare the security risks associated with publicly exposed information from both entities, without performing intrusive actions, and to generate a technical report with findings, risks, and recommendations.

## 📄 Instructions

1. **Selection of organizations:** Each group must choose a **public organization** (e.g., university, hospital, municipality) and a private organization (e.g., tech company, private clinic, ecommerce). Both must have their own web domain, be present in search engines, and have accessible open sources.

2. **OSINT collection phase:** Passively collect information about both entities using OSINT tools. Suggested categories:

    - Visible infrastructure: Subdomains (`dnsdumpster.com`, `crt.sh`, `Sublist3r`), IP addresses, and hosting.

    - Public emails and accounts: `theHarvester`, `hunter.io`

    - Internet-accessible services: `Shodan`, `Censys` to identify open ports, banners, technologies

    - Leaks and exposed credentials: `Have I Been Pwned`, `DeHashed` (only if allowed)

    - Indexed documents and paths: Use Google Dorks to locate sensitive files and unwanted pages (`filetype:`, `intitle:`, `inurl:`)

    - Social media profiles (optional): Presence on platforms, public comments, data exposure.



3. **Comparative analysis.** Complete a table with the key findings for each organization:

| Element                        | Public Entity        | Private Entity        |
|--------------------------------|---------------------|----------------------|
| Exposed subdomains             |                     |                      |
| Email addresses                |                     |                      |
| Devices on Shodan              |                     |                      |
| Leaks found                    |                     |                      |
| Indexed documents              |                     |                      |
| Identified risks               |                     |                      |

Answer:

- Which entity shows greater exposure and why?
- What passive security practices are evident?
- What risks are most relevant in each case?

4. **Final report.** The report must include:

1. Introduction
2. Methodology used
3. Results and evidence
4. Structured comparison
5. Mitigation recommendations
6. Critical conclusion


## ✅ Deliverables

- Technical report in PDF
- Comparative table (in the report or separately)
- Organized evidence (optional: attached folder)
- (Optional) Presentation of results in class


## Evaluation criteria

| Criteria                                 | Weight      |
|-------------------------------------------|-------------|
| Correct use of OSINT tools                | 30%         |
| Depth of comparative analysis             | 25%         |
| Quality of report and writing             | 20%         |
| Relevance of findings and risks           | 15%         |
| Improvement and mitigation proposals      | 10%         |



## 📝 License and use

This project is for academic use only and does not authorize the public exposure of real data without consent. Based on ethical cyber intelligence principles and responsible OSINT.
