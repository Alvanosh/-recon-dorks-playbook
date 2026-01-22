# 🔍 Google Dorking Playbook
![logo](logo.png)


A practical and ethical playbook for using Google Dorks in:
- Security reconnaissance
- Bug bounty programs
- OSINT investigations
- Educational research

> ⚠️ This repository is for **educational and authorized security testing only**.

---

## 📌 What is Google Dorking?
Google Dorking (Google Hacking) is the use of advanced search operators
to discover exposed information indexed by search engines.

---



## 📊 Google Dorking Command Table

You can paste this directly into `README.md` or a separate `google-dorks-table.md`.



| #  | Category          | Google Dork                             | What It Actually Finds                                  |
| -- | ----------------- | --------------------------------------- | ------------------------------------------------------- |
| 1  | Scope Control     | `site:example.com`                      | Restricts search to the target domain (ABSOLUTE BASICS) |
| 2  | Directory Listing | `intitle:"index of"`                    | Open directory listings                                 |
| 3  | Directory Listing | `intitle:"index of" "parent directory"` | Misconfigured servers                                   |
| 4  | Admin Panels      | `inurl:admin`                           | Admin panels & dashboards                               |
| 5  | Admin Panels      | `intitle:"Admin Login"`                 | Explicit admin login pages                              |
| 6  | Login Pages       | `inurl:login`                           | User login endpoints                                    |
| 7  | Login Pages       | `inurl:signin`                          | Alternative auth portals                                |
| 8  | Config Files      | `inurl:config`                          | Configuration files                                     |
| 9  | Config Files      | `filetype:xml site:example.com`         | XML configs, SSO, APIs                                  |
| 10 | Secrets           | `intext="DB_PASSWORD"`                  | Hardcoded database creds                                |
| 11 | Secrets           | `intext="API_KEY"`                      | Exposed API keys                                        |
| 12 | Secrets           | `intext="password="`                    | Plaintext password leaks                                |
| 13 | Git Exposure      | `inurl:.git/config`                     | Exposed Git repositories                                |
| 14 | Git Exposure      | `intitle:"index of" ".git"`             | Full Git directory leaks                                |
| 15 | Backups           | `filetype:bak OR filetype:old`          | Backup files                                            |
| 16 | Backups           | `filetype:zip site:example.com`         | Zipped backups                                          |
| 17 | Logs              | `filetype:log site:example.com`         | Server & error logs                                     |
| 18 | Errors            | `intext:"Fatal error"`                  | PHP / app crashes                                       |
| 19 | Errors            | `intext:"stack trace"`                  | Debug traces                                            |
| 20 | APIs              | `inurl:api site:example.com`            | API endpoints                                           |
| 21 | APIs              | `inurl:swagger OR intitle:"Swagger UI"` | Public API docs                                         |
| 22 | Cloud             | `site:s3.amazonaws.com example`         | Public AWS S3 buckets                                   |
| 23 | Cloud             | `site:blob.core.windows.net example`    | Azure blob storage                                      |
| 24 | Cloud             | `site:storage.googleapis.com example`   | Google Cloud storage                                    |
| 25 | Firebase          | `site:firebaseio.com`                   | Open Firebase databases                                 |



## ⚠️ VERY IMPORTANT (don’t skip this)


```md
> ⚠️ These Google dorks are provided for **educational purposes only**.
> Use them **only on assets you own or have explicit permission to test**,
> such as bug bounty program scopes.
```

---
## 📌 EXAMPLES
```md
site:example.com
```
![site](site.png)

```md
site:tesla.com filetype:pdf
```
![filetype](filetype.png)


```md
site:linkedin.com inurl:"signup"
```
![inurl](inurl.png)


```md
site:tryhackme.com intitle:admin
```
![intitle](intitle.png)
