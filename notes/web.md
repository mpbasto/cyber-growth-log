# 🌐 Web Fundamentals Cheat Sheet

## 🧭 DNS Resolution Stages

When you type a domain like `example.com` in your browser, here’s what happens to resolve it to an IP address:

1. **Browser Cache**

   - Checks if the domain’s IP is already cached locally.

2. **Operating System Cache**

   - If not in browser, the OS checks its DNS cache.

3. **Router/Local Network**

   - Your router may store recent DNS lookups.

4. **ISP DNS Server**

   - If not resolved locally, the DNS query goes to your Internet Service Provider.

5. **Recursive Resolution**

   - If ISP doesn't have the answer:
     - It queries a **Root DNS Server**
     - Then a **TLD Server** (like `.com`)
     - Then the **Authoritative Name Server** for `example.com`

6. **Response Returned**
   - Once resolved, the IP is returned and cached at each level for faster future use.

---

## 🖥️ Client vs Server Overview

| Aspect        | **Client**                            | **Server**                                    |
| ------------- | ------------------------------------- | --------------------------------------------- |
| Role          | Initiates requests                    | Responds to requests                          |
| Location      | User’s device (browser, app)          | Remote machine (website backend)              |
| Examples      | Chrome, Firefox, Postman, mobile apps | Apache, Nginx, Flask, Node.js, etc.           |
| Data Flow     | Sends HTTP requests                   | Processes requests, sends back HTTP responses |
| Key Languages | HTML, CSS, JS (runs in browser)       | Python, PHP, Java, etc. (runs on server)      |
| Perspective   | “What the user sees & does”           | “How the app works under the hood”            |

> 💡 Think of the client as the **restaurant customer** and the server as the **kitchen** taking and fulfilling their order.
