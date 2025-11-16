# Phishing Email Analysis — Revolut T&C Update (Task 2)

**Source file:** email.txt

## Summary
The message impersonates Revolut and instructs the user to accept updated Terms & Conditions or face account suspension. Technical header analysis and the body’s social-engineering cues indicate this is a phishing attempt.

## Evidence / Findings
1. **From:** "Revolut" <no-reply@revolut-example.com>
   - Domain `revolut-example.com` is not official `revolut.com`.

2. **Return-Path:** <no-reply@revolut-example.com>

3. **Received headers** (earliest first):
(Note: Example ip have been used)
   - from [192.0.2.45] (unknown [192.0.2.45]) by suspicious-mailer.relay ...
   - from suspicious-mailer.relay (198.51.100.23) by mx.example.org ...
   - *Why suspicious:* unknown relays, test-range IPs and hostnames; not Revolut’s mail servers.

4. **Authentication-Results:** `spf=fail; dkim=none; dmarc=fail`
   - *Why suspicious:* sending IP not authorized by domain, no DKIM signature, DMARC fails → strong evidence of spoofing.

5. **Suspicious link(s):**
   - `http://revolut-verify.example.com/review` (do not visit)

6. **Social engineering techniques:**
   - Urgent deadline and threat of account suspension to force action.

## Recommendation
- Do NOT click links or open attachments.
- Report the message as phishing to your email provider and to Revolut via official channels.
- Access account only through the official app or by typing `https://revolut.com` manually.
- Delete the message.

## Appendix
- headers.txt
- email.txt
- quick_findings.txt

