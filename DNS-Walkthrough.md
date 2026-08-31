# How the Internet Finds a Website: A Simple DNS Walkthrough

Have you ever wondered what actually happens behind the scenes when you type a web address like `minelap.netlify.app` into your browser? 

Computers don't naturally understand human words. They speak in numbers called **IP addresses** (like `192.0.2.1`). The **DNS (Domain Name System)** is the internet’s global address book—it translates friendly human website names into the numerical IP addresses that computers use to find each other.

Here is a step-by-step breakdown of what happens in just a fraction of a second:

---

## 1. The 4 Steps of a DNS Request

### Step 1: The Request (The Resolver)
When you type an address into your browser, the browser first asks a **Recursive Resolver** (usually operated by your Internet provider or public DNS services like Cloudflare `1.1.1.1`): *"Do you know where minelap.netlify.app lives?"*

### Step 2: The Root Nameserver
If the resolver doesn't already have the address saved in its memory, it asks the **Root Nameserver**. The Root server is like the main index of the internet. It replies: *"I don't know the exact site, but I know who manages all `.app` websites."*

### Step 3: The TLD (Top-Level Domain) Nameserver
The resolver then contacts the **.app TLD Nameserver**. The TLD server responds: *"I know where Netlify's domain servers are. Go ask them!"*

### Step 4: The Authoritative Nameserver (The Final Answer)
Finally, the resolver reaches Netlify's **Authoritative Nameserver**. This server holds the exact, final record for `minelap.netlify.app`. It gives back the precise numerical IP address of the server hosting the website files.

The resolver hands this IP address back to your browser, your browser downloads the website files over a secure (HTTPS) connection, and the page appears on your screen!

---

## 2. What is a CNAME Record?

An **A Record** connects a domain directly to a static IP address (e.g., `mysite.com` $\rightarrow$ `192.0.2.1`).

A **CNAME (Canonical Name) Record**, on the other hand, acts like a nickname or forwarding rule. It maps one domain name to another domain name instead of an IP.

### Real-World Example:
If you purchase a custom domain in the future (like `mineladev.com`) and want it to display your Netlify site:
* You would add a CNAME record: `www.mineladev.com` $\rightarrow$ `minelap.netlify.app`.
* When a visitor types `www.mineladev.com`, the DNS system automatically redirects the lookup to Netlify’s servers, serving your content while keeping your custom URL in the address bar.