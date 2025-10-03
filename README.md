# Domain-Names



<h2>Description</h2>
In this lab, I explored the identification and classification of  domain names used by attackers to understand their role in the attack lifecycle. This helps in assessing which indicators are easier or harder to change, enabling more effective detection and defense strategies.


<h2>Utilities Used</h2>

- <b>ANY.RUN interactive online malware analysis sandbox</b> 
  



<h2>Lab walk-through:</h2>

<p align="center">
ANY.RUN module executed the malware sample in a sandboxed environment, capturing network activity, C2 domain communications, dropped files, and process behavior. Reviewing indicators for further analysis:
  
<br/>
<img src="https://i.imgur.com/uZUJYxU.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewed HTTP requests samples, including callbacks and files retrieved from web servers.
<br />
<img src="https://i.imgur.com/T4s3VUP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewed all sample-initiated network connections, such as C2 communications and file uploads/downloads 

<br/>
<img src="https://i.imgur.com/PZjO6i4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Displays DNS queries by the sample, useful for identifying C2 communications or sandbox detection attempts.
<br/>
<img src="https://i.imgur.com/2D0DIIq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewed report, indicators showing suspicious domain requests helps identify malicious activity like C2 communication or phishing. Malware may use DNS requests or URL shorteners to hide destinations or evade detection. Extracted domains should be documented as IOCs and blocked or monitored:  <br/>
<img src="https://i.imgur.com/zjIvMaL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />





<h2>Learned Outcomes</h2>

Learned to review DNS and HTTP requests, identify malicious infrastructure, safely handle shortened URLs, and document findings for incident response.



<h2>Final Comments</h2>

This lab showed that the malware tried to communicate with several suspicious domains and used techniques like URL shortening to hide its activity. This confirms the system was exposed to potentially harmful activity.

Recommendations

Block the identified domains and shortened URLs at the firewall and DNS.

Isolate any affected computers and scan them for malware.

Add the identified domains and file hashes to monitoring tools to catch future attempts.

Remind users not to click on unknown links or files.

Keep systems and applications up to date to reduce vulnerabilities.



<h2>TryHackMe Lab Completion</h2>
<br/>
<img src="https://i.imgur.com/gyXSiIf.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />



