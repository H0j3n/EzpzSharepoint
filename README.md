# EzpzSharepoint

### Checklist

```bash
1. Check if can access underneath
-> _vti_inf.html
-> _vti_bin/
-> _vti_pvt/
-> _vti_bin/spsdisco.aspx

2. Check Viewstate encrypted or not

3. Check if _layouts folder can be access anonymously

4. Check if X-Frame-Options available or not (Clickjacking)

5. Check any Stack Trace and Errors Disclosure

6. Insufficient Transport Layer Protection (SSL)
```

### CVE/Exploit Related

1. **CVE-2021-31181**
- https://www.zerodayinitiative.com/blog/2021/6/1/cve-2021-31181-microsoft-sharepoint-webpart-interpretation-conflict-remote-code-execution-vulnerability

2. **CVE-2021-27076**

- https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-27076

3. **CVE-2020-0932**
- https://www.zerodayinitiative.com/blog/2020/4/28/cve-2020-0932-remote-code-execution-on-microsoft-sharepoint-using-typeconverters

4. **CVE-2019-0604**
- https://www.rapid7.com/db/vulnerabilities/msft-cve-2019-0604/

### Related 
- https://kvssankararao.blogspot.com/2016/11/protecting-sharepoint-server.html?m=1
- https://the-infosec.com/2017/04/18/penetration-testing-sharepoint/
- https://www.defcon.org/images/defcon-11/dc-11-presentations/dc-11-Shannon/presentations/dc-11-shannon.pdf
- https://www.ethicalhacker.net/forums/topic/pen-testing-sharepoint/
- https://trojand.com/cheatsheet/Methodologies/Sharepoint.html
- https://vladilen.com/content/sharepoint-security-and-penetration-testing/
- https://www.compass-security.com/fileadmin/Research/Presentations/2013-03_beer-talk_sharepoint-security-revealed.pdf

### Understanding Sharepoint
- https://sharepointmaven.com/the-anatomy-of-a-sharepoint-url/

### References
- http://www.office365security.com/sharepoint-security-policy-checklist/
- https://docs.microsoft.com/en-us/sharepoint/security-for-sharepoint-server/security-hardening
- https://cipherpoint.com/blog/sharepoint-list-security/
- https://cipherpoint.com/blog/sharepoint-security-audit-review/
- https://silo.tips/download/maximizing-sharepoint-security-whitepaper-v10-12-2015