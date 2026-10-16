# Cross-Site-Scripting(XSS)

# 1. Introduction
Cross-Site Scripting (XSS) is a web application vulnerability that allows attackers to inject malicious scripts, usually JavaScript, into webpages viewed by users.

## 2. Types of XSS

### A. Reflected XSS
Reflected XSS occurs when user input is immediately returned in a webpage without proper validation or encoding.

**Example payload:**
<script>alert('Reflected XSS')</script>

**Testing steps:**
1. Open an authorized vulnerable test application.
2. Enter the payload into a search field or URL parameter.
3. Submit the input.
4. Check whether the browser executes the script.
### B. Stored XSS
Stored XSS occurs when malicious input is saved by an application and executes when the stored content is displayed to users.

**Example payload:**
<script>alert('Stored XSS')</script>

**Testing steps:**
1. Open a practice application's comment or message form.
2. Enter the payload and submit it.
3. Reload the page.
4. Check whether the script executes when the saved content is displayed.

## 3. Impact of XSS
- Unauthorized actions performed through a victim's browser.
- Exposure of sensitive information accessible to injected scripts.
- Modification of webpage content.
- Phishing or misleading content displayed to users.

The actual impact depends on the application, browser protections, and the privileges of the affected user.

## 4. Prevention
- Encode output according to its HTML, attribute, URL, or JavaScript context.
- Prefer safe DOM methods such as `textContent` instead of unsafe `innerHTML` for plain text.
- Validate input appropriately.
- Use a Content Security Policy (CSP) as an additional security layer.
- Use secure frameworks and avoid unsafe HTML rendering.
- Do not rely on input validation alone to prevent XSS.

**Disclaimer:** Perform security testing only on applications you own or have explicit permission to test.
