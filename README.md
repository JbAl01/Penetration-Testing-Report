# Penetration-Testing-Report
This is a penetration report as a part of my college. The exam was based on a 4 hour session with hands-on penetration testing. Where the students has to find as many vulnerabilities as they can. Afterwards we got a timeframe of 5 days, to write a report which one section has to be a detailed section with one of the vulnerabilities we found. This was a capture the flag type of exam, for each vulnerability found it will prompt with an flag that we have to submit. The target was Harrow AS, which is a website to upload pictures and buy them from people there. We learned OWASP Top 10, so we have to use those to find CWE and find vulnerabilitiies.


One of the vulnerabilties I found quickly was manipulation of ID in the URL, meaning there is no proper access control. And a leak code came up, meaning it was vulnerable to this.
<img width="694" alt="v01-e1" src="https://github.com/user-attachments/assets/d64494d1-9006-4d6c-bf8b-38cbe3098bf4" />

I went to other pages, and tried for XSS exploits on each page and found one in a vulnerable page

<img width="600" alt="v02-e1" src="https://github.com/user-attachments/assets/0c000a8d-9dd2-497c-bfa8-ecd4cb8b96e4" />

And it was vulnerable :D
I explored other parts of the site and inspected the source code to see if anything looked suspicious. I came across a PNG image link that stood out. Out of curiosity, I accessed the link—even though it seemed like it should’ve been restricted, since the image wasn’t displayed anywhere else on the site. Surprisingly, I was able to view the image directly, and it turned out to be a high-resolution, paid asset that I accessed for free. This vulnerability is called Broken Access Control, or unprotected file/resource endpoint.

<img width="900" alt="v03-e1" src="https://github.com/user-attachments/assets/4053ee3e-4f08-402a-ae20-4f8c5dc0ae1e" />
aa
<img width="800" alt="v03-e2" src="https://github.com/user-attachments/assets/2d8d4e55-0904-4075-a349-c5cd1c6cb7f3" />
aa
<img width="981" alt="v03-e3" src="https://github.com/user-attachments/assets/498f9daf-b2ba-471c-8af7-37f6d3a3ab26" />.

SQL Injection was found, and I felt it was obligatory to look for it and expose it.

<img width="500" alt="v04-e1" src="https://github.com/user-attachments/assets/e89fc8ae-118f-4c54-907a-8147ac404433" />

<img width="908" alt="v04-e2" src="https://github.com/user-attachments/assets/d394cee2-b51b-477a-bc4b-23472985d799" />




