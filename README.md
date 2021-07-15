# EzpzSharepoint

### Disclaimer

This is my note taking on Sharepoint . Every information in here is a collection from all of the references. Anything news related to Sharepoint will be updated in here.

### Information


| Folder   |      Information  |
|----------|:-------------:|
| _app_bin |  The _app_bin folder was designed to hold application assemblies which were previously installed in _layouts/bin.  WebPart assemblies are *not* supposed to be installed in this folder. Put your assemblies in GAC or the bin, but not the _app_bin. | 
| _vti_pvt |    This folder is used by FrontPage Extensions/SharePoint Designer. It contains Legacy FrontPage Server Extensions files/folders. The reason for having these folders is that they provide the underlying infrastructure files for the many features SharePoint Designer provides.   | 
| Bin | Contains compiled assemblies (.dll files) for controls, components, or other code that you want to reference in your application. Any classes represented by code in the Bin folder are automatically referenced in your application. | 
| App_Browsers | Contains browser definitions (.browser files) that ASP.NET uses to identify individual browsers and determine their capabilities. | 
| App_GlobalResources | Contains resources (.resx and .resources files) that are compiled into assemblies with global scope. Resources in the App_GlobalResources folder are strongly typed and can be accessed programmatically. | 
| Wpresources | Contains configuration file for Web Parts| 

### User Enumeration
1. Passive User Enumeration With **OneDrive **
- https://www.trustedsec.com/blog/achieving-passive-user-enumeration-with-onedrive/
2. Sharepoint User Enumeration In **userdisp.aspx**
- https://www.acunetix.com/vulnerabilities/web/sharepoint-user-enumeration/

```bash
_layouts/userdisp.aspx
_layouts/userdisp.aspx?Force=True&id=1
```
3. Sharepoint User Enumeration In **editform.aspx**

```bash
-> Try check if editform.aspx can be open or not.
-> If it can be access, follow the steps below:

1. Location => /pages/forms/editform.aspx
2. Inside Contact write any characters atleast 3 characters. Then it will list out several recommendations of users to us. One of the tricks that we found is to put 2 spaces add with one chracter.
3. Examples:
	- "  a"
	- "  b"
	- "  c"
4. You might only get a few list. So intercept the request using Burpsuite and change MaximumEntitySuggestions to high numbers.
```

### Can't access viewlsts.aspx?

```bash
-> Try check if editform.aspx can be open or not.
-> If it can be access, follow the steps below:

1. Location => /pages/forms/editform.aspx
2. Click on "Click here to insert a picture from Sharepoint"
3. Click on browse in Hyperlink
4. We can view the Site Content almost same like viewlsts.aspx
```

### CVE/Exploit Related

1. **CVE-2021-31181**
- https://www.zerodayinitiative.com/blog/2021/6/1/cve-2021-31181-microsoft-sharepoint-webpart-interpretation-conflict-remote-code-execution-vulnerability

2. **CVE-2021-27076**
- https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-27076

3. **CVE-2020-0932**
- https://www.zerodayinitiative.com/blog/2020/4/28/cve-2020-0932-remote-code-execution-on-microsoft-sharepoint-using-typeconverters

4. **CVE-2020-1147**
- https://www.exploit-db.com/exploits/48747

5. **CVE-2019-0604**
- https://www.rapid7.com/db/vulnerabilities/msft-cve-2019-0604/

### Understanding Sharepoint
- https://sharepointmaven.com/the-anatomy-of-a-sharepoint-url/
- https://mohitvash.wordpress.com/2011/06/17/microsoft-sharepoint-applicationpages-dll/
- https://github.com/MicrosoftDocs/OfficeDocs-Support/tree/public/SharePoint/SharePointServer
- https://www.sharepointdiary.com/
- https://mstechtalk.com/sharepoint-important-urls/

### Tools Related
- https://github.com/0xdevalias/sparty

### References
- http://www.office365security.com/sharepoint-security-policy-checklist/
- https://docs.microsoft.com/en-us/sharepoint/security-for-sharepoint-server/security-hardening
- https://cipherpoint.com/blog/sharepoint-list-security/
- https://cipherpoint.com/blog/sharepoint-security-audit-review/
- https://silo.tips/download/maximizing-sharepoint-security-whitepaper-v10-12-2015
- https://www.sharepointdiary.com/2020/05/sharepoint-online-link-to-document-download-instead-of-open.html
- https://social.technet.microsoft.com/Forums/sharepoint/en-US/89393b55-df36-4996-b8d0-4bb12a46b433/specific-folders-virtual-directories-for-a-sharepoint-application?forum=sharepointadminlegacy
- https://www.slideshare.net/IanNaumenkoCISSP/hackingsharepointfinal-59552814
- https://kvssankararao.blogspot.com/2016/11/protecting-sharepoint-server.html?m=1
- https://the-infosec.com/2017/04/18/penetration-testing-sharepoint/
- https://www.defcon.org/images/defcon-11/dc-11-presentations/dc-11-Shannon/presentations/dc-11-shannon.pdf
- https://www.ethicalhacker.net/forums/topic/pen-testing-sharepoint/
- https://trojand.com/cheatsheet/Methodologies/Sharepoint.html
- https://vladilen.com/content/sharepoint-security-and-penetration-testing/
- https://www.compass-security.com/fileadmin/Research/Presentations/2013-03_beer-talk_sharepoint-security-revealed.pdf