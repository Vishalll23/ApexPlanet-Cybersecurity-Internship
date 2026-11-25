# Burp Suite – Web Application Security Testing

## 1. Objective
To understand how Burp Suite intercepts HTTP requests and allows security testers to inspect communication between a browser and a web server.

## 2. Introduction
Burp Suite is a web application security testing platform developed by PortSwigger.

It helps security professionals:
- Intercept HTTP requests and responses.
- Inspect request headers and parameters.
- Analyze server responses.
- Identify potential web application security issues.

## 3. Tools and Environment
- Kali Linux
- Burp Suite Community Edition v2026.3.2
- Burp's built-in Chromium browser
- Metasploitable 2
- VirtualBox Host-Only Network

## 4. Practical 1 – Intercepting HTTP Requests

**Objective:** Intercept and inspect an HTTP request using Burp Proxy.

Target:

`http://192.168.56.102/`

Steps performed:
1. Started Burp Suite.
2. Opened Proxy → Intercept.
3. Launched the built-in browser.
4. Accessed the Metasploitable web server.
5. Observed the intercepted HTTP request.
6. Forwarded the request to the server.

**Observed request details:**

| Field | Value |
|---|---|
| Method | GET |
| Host | 192.168.56.102 |
| Protocol | HTTP/1.1 |
| URL | / |
| Connection | keep-alive |

## 5. Practical 2 – Analyzing HTTP Responses

**Objective:** Inspect the response returned by the web server.

Steps performed:
1. Opened Proxy → HTTP history.
2. Selected the request for the Metasploitable web server.
3. Opened the Response tab.
4. Inspected the server response.

Information examined:
- HTTP status code
- Response headers
- Content-Type
- HTML response body

## 6. Important Burp Suite Features

| Feature | Purpose |
|---|---|
| Proxy | Intercepts HTTP/HTTPS traffic |
| HTTP History | Stores captured requests and responses |
| Repeater | Allows manual modification and resending of requests |
| Intruder | Automates customized request testing |
| Decoder | Encodes and decodes data |
| Comparer | Compares two pieces of data |

## 7. Learning Outcomes
- Understood how Burp Proxy works.
- Successfully intercepted an HTTP GET request.
- Learned to inspect HTTP request headers.
- Examined the corresponding server response.
- Understood the role of Burp Suite in web application security testing.

## 8. Screenshots
Screenshots are stored in:

`Task-1/Tools/Screenshots/`

- `16-Burp-HTTP-Request-Intercept.png`
- `17-Burp-HTTP-Response.png`

## 9. Conclusion
Burp Suite Community Edition was used to intercept and inspect HTTP communication with the Metasploitable test server. This practical demonstrated how web application security testers analyze requests and responses to understand potential security weaknesses.

All testing was performed within an isolated, authorized lab environment.
