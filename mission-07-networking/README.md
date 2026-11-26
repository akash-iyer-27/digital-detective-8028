# Mission 7 — How Computers Communicate

## 1. Task / Objective

The aim of this mission was to explain basic network types and concepts, observe connectivity and DNS lookup information using Terminal, and describe what happens when a website opens.

## 2. Work Completed

- Explained eight network concepts in my own words with examples.
- Checked connectivity to `example.com` and looked up its IP address.
- Answered the questions about connectivity tests and DNS.
- Wrote a 7-step explanation of what happens when a website opens.
- Saved privacy-safe output in `evidence/mission-07-network-output.txt`.

## 3. Commands / Tools Used

| Command | Purpose |
|---|---|
| `ping -c 4 example.com` | Sends 4 test packets to a public website to check that it can be reached, and shows how long the replies take. |
| `nslookup example.com` | Looks up the IP address that the domain name points to, showing only the answer. |

**Tools used:** Terminal and a text editor.

## 4. My Understanding

### Task 7.1 — Network concepts

| Concept | Explain it in your own words | Example |
| --- | --- | --- |
| LAN | A network that connects devices in one small area, so they can share files and internet access. | My home Wi-Fi, or the network in a computer lab. |
| MAN | A network that connects devices across a city or a large campus. | A network linking all the buildings of a college campus. |
| WAN | A network that spreads across cities, countries or continents. | The internet. |
| DNS | A system that turns a website name into the IP address a computer needs to find it. | Turning `example.com` into an IP address. |
| Router | A device that connects networks and sends data to the right place. | The Wi-Fi router that connects my home network to the internet. |
| Protocol | A set of rules that devices follow so they can understand each other. | HTTPS for websites. |
| Packet switching | Data is cut into small packets that travel separately and are put back together at the destination. | A photo sent in a chat is split into packets that may take different routes. |
| Client-server | A client asks for something and a server answers with it. | My browser (client) requests a page from a web server. |

### Task 7.2 — Observing network information

**Connectivity test:** I ran `ping -c 4 example.com`. `<<e.g. 4 packets were sent and 4 were received with 0.0% packet loss, and the average reply time was about 3 ms>>`.

**DNS lookup:** I ran `nslookup example.com`. It printed `<<the IP address(es) you saw>>`.

**What does a connectivity test help me check?**
It checks whether my computer can reach another computer over the network, whether any packets are lost, and how long the replies take.

**What information does a DNS lookup display?**
It shows the IP address that a domain name points to.

**What is the role of DNS when I enter a website name in a browser?**
Computers find each other using IP addresses, not names. When I type a website name, DNS looks up the IP address so the browser knows which server to contact.

### Task 7.3 — What happens when I open a website?

1. I type a website address into my browser. The browser is the **client**, and it needs to contact the website's **server**.
2. The browser asks **DNS** to turn the domain name into an IP address.
3. The browser uses a **protocol**, usually HTTPS, to send a request for the page to that IP address.
4. The request leaves my device and reaches my **router**, which passes it on through the internet. The data is split into **packets** that travel across several networks.
5. The packets reach the web **server**, which finds the page that was asked for.
6. The server sends its response back as packets, through the router, to my computer.
7. My browser puts the packets together and displays the page on my screen.

## 5. Difficulties Faced

No major difficulties

## 6. How I Resolved Them

Not applicable

## 7. Evidence / Files

- `evidence/mission-07-network-output.txt`: output of `ping` and `nslookup`, with no personal network details.
- `mission-07-networking/README.md`: this file.

## 8. Commit Details

- **Commit message:** `Explain networking concepts and website communication`
- **Status:** Pushed to GitHub.
- **Verification:** Checked the repository on GitHub to confirm the README, evidence file and commit are visible.