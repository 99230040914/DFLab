# Ex.No.4   MHA (Mail Header Analyzer)
## Aim :
- The aim is to use a Mail Header Analyzer (MHA) to trace an email's origin and verify its authenticity by examining its header for signs of spoofing.
## Procedure
### Step 1: Get the Email Header
- First, you need to copy the full, raw header from the email.

- Gmail: Open the email, click the three dots (⋮), and select Show original.
<br>
<br>
<img width="1903" height="882" alt="Screenshot 2025-09-09 000325" src="https://github.com/user-attachments/assets/3e47f0ba-d6e1-47e3-b4ee-7c5626c5694e" />

<br>
<br>


- Select all the text in the header and copy it.

<br>
<img width="1909" height="961" alt="Screenshot 2025-09-09 000401" src="https://github.com/user-attachments/assets/69ecfa31-e2a8-4cba-bff2-f7076a06706e" />

<br>
<br>

### Step 2: Use a Mail Header Analyzer (MHA)
- The easiest way to analyze the header is with an online tool.

- Navigate to a site like MXToolbox Email Header Analyzer.
 <br>
<br>

  <img width="1914" height="879" alt="Screenshot 2025-09-09 000802" src="https://github.com/user-attachments/assets/0600cce3-11e1-429c-a2a9-cd6d7f9bc49b" />

<br>
<br>

- Paste the entire header you copied into the analysis box.
<br>
<br>

Click the "Analyze" button to get a parsed, easy-to-read report.
<br>
<br>

<img width="1910" height="877" alt="Screenshot 2025-09-09 000900" src="https://github.com/user-attachments/assets/efeb1f30-557e-49cc-8228-dfc079485b02" />

### Step 3: Analyze The Report
- This is the most critical step. In the analyzer's report, look for the SPF, DKIM, and DMARC results.
### Review the Overall Delivery Summary
- First, look at the high-level summary to get an immediate sense of the email's status.

- Check DMARC Compliance: The report shows the email is DMARC Compliant. This is the most important overall result.

- Check SPF Status: Both SPF Authenticated and SPF Alignment passed. This means the sending server was authorized.

- Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated failed (❌). This is a critical finding and indicates a problem with the email's digital signature.
<br>
<br>
<img width="1915" height="852" alt="Screenshot 2025-09-09 001025" src="https://github.com/user-attachments/assets/da8dfde9-da25-41d8-9a54-e69f6ce8d748" />

<br>
<br>

### Investigate the SPF Record and Email Path
- Next, verify why the SPF check passed.

- Examine the SPF Record: The SPF record for the domain is v=spf1 include:mailgun.org ~all. This record explicitly authorizes servers from Mailgun to send emails on its behalf.

- Trace the Relay Information: The delivery path shows the email was sent from m241-136.mailgun.net.

- Conclusion: Since the email came from a Mailgun server, which is authorized in the SPF record, the SPF check passed.
  <br>
  <br>
<img width="1906" height="413" alt="Screenshot 2025-09-09 001056" src="https://github.com/user-attachments/assets/c4d270ca-ecd7-4a5c-9be2-fca8e4c2616c" />

<br>
<br>

### Analyze the DKIM Failure

<br>
<img width="1849" height="826" alt="Screenshot 2025-09-09 001105" src="https://github.com/user-attachments/assets/bdfa0fb5-4ec7-42fc-8f36-05bf3b1c0393" />
