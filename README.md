# cybersec-writeups
---
## OverlayFS
https://ssd-disclosure.com/ssd-advisory-overlayfs-pe/
#### Want to know more about OverlayFS?
https://yagrebu.net/unix/rpi-overlay.md - Read only root file system with overlayfs to allow applications to run normally.
https://wiki.archlinux.org/index.php/Overlay_filesystem - The Arch Wiki's page on OverlayFS (I don't use Arch BTW)
#### Want to know more about this specific CVE?
https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3493 - Mitre's CVE entry for this vulnerability, which includes many further links.
https://ssd-disclosure.com/ssd-advisory-overlayfs-pe/ - This is where we got the PoC code, and it explains the vulnerability very well.

---

## Moniker Link ([CVE-2024-21413](https://github.com/advisories/GHSA-9mp4-h7q5-2rgq))
#### Microsoft Outlook Remote Code Execution Vulnerability

https://www.cve.org/CVERecord?id=CVE-2024-21413
https://msrc.microsoft.com/update-guide/en-US/vulnerability/CVE-2024-21413
https://learn.microsoft.com/en-us/windows/win32/com/url-monikers

**What kind of security feature could be bypassed by successfully exploiting this vulnerability?**

Successful exploitation of this vulnerability would allow an attacker to bypass the Office Protected View and open in editing mode rather than protected mode.

**According to the CVSS metrics, successful exploitation of this vulnerability could lead to major loss of confidentiality (C:H), integrity (I:H), and availability (A:H). What does that mean for this vulnerability?**

An attacker who successfully exploited this vulnerability could gain high privileges, which include read, write, and delete functionality.

**If I am running Office 2016 (32-bit edition) or Office 2016 (64-bit edition, what do I need to do to be protected from this vulnerability?**

To be protected, customers running Office 2016 need to install all the updates listed for their edition in the following tables.

**For Office 2016 (32-bit edition)**:

| Product | Article | Download | Build Number |
| --- | --- | --- | --- |
| Microsoft Office 2016 (32-bit edition) | [5002537](https://support.microsoft.com/help/5002537) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=3f798cca-1d11-494e-82a5-f8e8cbe4d716) | 16.0.5435.1001 |
| Microsoft Office 2016 (32-bit edition) | [5002467](https://support.microsoft.com/help/5002467) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=0019c7f4-e4f2-4741-8cfb-0fd2311b71f4) | 16.0.5435.1001 |
| Microsoft Office 2016 (32-bit edition) | [5002522](https://support.microsoft.com/help/5002522) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=eced3839-7e06-43be-a013-ff34c4a3e4a7) | 16.0.5435.1001 |
| Microsoft Office 2016 (32-bit edition) | [5002469](https://support.microsoft.com/help/5002469) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=8315c33e-7682-4031-a323-f8c01c53dac1) | 16.0.5435.1001 |
| Microsoft Office 2016 (32-bit edition) | [5002519](https://support.microsoft.com/help/5002519) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=f6e4a256-d7fb-4ad0-a998-d3cdd5ea4bd8) | 16.0.5435.1001 |

**For Office 2016 (64-bit edition)**:

| Product | Article | Download | Build Number |
| --- | --- | --- | --- |
| Microsoft Office 2016 (64-bit edition) | [5002537](https://support.microsoft.com/help/5002537) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=0754e80a-a661-4e4c-b876-7288e83d0e26) | 16.0.5435.1001 |
| Microsoft Office 2016 (64-bit edition) | [5002467](https://support.microsoft.com/help/5002467) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=e80c5e98-5fd0-45d2-931c-4ebb126db870) | 16.0.5435.1001 |
| Microsoft Office 2016 (64-bit edition) | [5002522](https://support.microsoft.com/help/5002522) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=2b476112-870d-451c-a7d7-e513e72ec383) | 16.0.5435.1001 |
| Microsoft Office 2016 (64-bit edition) | [5002469](https://support.microsoft.com/help/5002469) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=cfd78b2e-736d-4e29-83a7-44699e8a289c) | 16.0.5435.1001 |
| Microsoft Office 2016 (64-bit edition) | [5002519](https://support.microsoft.com/help/5002519) | [Security Update](https://www.microsoft.com/download/details.aspx?familyid=96a56f04-fed0-4743-b518-23b904e9368e) | 16.0.5435.1001 |

**Is the Preview Pane an attack vector for this vulnerability?**

Yes, the Preview Pane is an attack vector.

**How could the attacker exploit this vulnerability?**

An attacker could craft a malicious link that bypasses the Protected View Protocol, which leads to the leaking of local NTLM credential information and remote code execution (RCE).

---
