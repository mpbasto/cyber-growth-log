# Lab: Capture HTTP Requests

**Date:** 2025-05-28
**Tool:** Wireshark  
**Topic:** Follow HTTP Stream

## 🧠 Goal

Understand how HTTP requests and server reponses (like 301 redirects) behave over the network.

## 🔍 What I Did

- Visited `http://neverssl.com` in browser
- Captured traffic using Wireshark
- Applied `http` filter
- Used **Follow HTTP Stream** to inspect full request/response exchange

## 📦 Packet Findings

- Initial request: `GET /online HTTP/1.1`
- Server response: `HTTP/1.1 301 Moved Permanently` → Redirected to `http://shiningtranscendentbeautifulmelody.neverssl.com/online/`
- Browser automatically re-sent GET request
- Final response: `HTTP/1.1 200 OK` with HTML content`
- Saw full plaintext headers and page content in stream view

## ⚠️ Surprises

- Learned that `301` redirects are silently followed by browsers
- Everything (including headers) was visible - no encryption at all
- Useful to see how one action can generate multiple HTTP requests
