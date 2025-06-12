# 🌐 Lab: Web Request Flow

**Date:** 2025-06-12  
**Topic:** Visualising a Simple HTTP Request Flow

---

## 🧭 Request Flow Diagram (Client → DNS → Web Server)

```plaintext
+------------+           +------------------+          +------------------+
|            |           |                  |          |                  |
|   Browser  +---------> |   DNS Resolver   +--------> |  Web Server IP   |
| (Client)   |  (1) URL  | (gets IP for URL)|          |   identified     |
|            |           |                  |          |                  |
+------------+           +------------------+          +------------------+

        (2) Server IP returned ←←←←←←←←←←←←←←←←←←←←←←

+------------+                                         +------------------+
|            |                                         |                  |
|   Browser  +---------------------------------------->+   Web Server     |
| (Client)   |     (3) Sends HTTP GET/POST request     |  (Apache, Nginx) |
|            |                                         |                  |
+------------+                                         +------------------+

                 ←←←←←←←←← (4) HTTP Response (HTML, JSON, etc.)
```

## 🔍 Description

1. User enters URL in the browser (e.g., example.com).

2. DNS resolution happens in stages — from cache → DNS resolver → authoritative server → returns IP.

3. Browser sends HTTP request to the resolved IP address (typically port 80 for HTTP or 443 for HTTPS).

4. Web server responds with content (e.g., HTML, JSON API, redirect).
