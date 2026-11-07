<p align="center">
  <img src="assets/WebRecon.png" alt="WebRecon" width="560">
</p>

<h3 align="center">Recon, planned step by step.</h3>


<p align="center">
  Enter one domain. Get an ordered recon workflow with copy-ready commands, expected results,<br>
  a visual attack-surface map and progress tracking. Built for bug bounty hunters and web pentesters.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Free%20%C2%B7%20Runs%20in%20your%20browser%20%C2%B7%20No%20sign--up-22c55e?style=flat-square" alt="Free, runs in your browser, no sign-up">
</p>

<h2 align="center">Start your recon with great METHODOLOGY. <sub>Stop guessing.</sub></h2>

<p align="center">
  ✅ <b>Ordered workflow</b> from subdomains to vulnerability checks<br>
  ✅ <b>Copy-ready commands</b> with every flag explained<br>
  ✅ <b>Progress you can trust</b>, saved per target
</p>

<p align="center">
  🌐 <a href="https://webrecon.xyz"><b>webrecon.xyz</b></a>
</p>

<p align="center">
  <a href="https://webrecon.xyz"><img src="https://img.shields.io/badge/%F0%9F%8C%90%20Website-webrecon.xyz-22c55e?style=for-the-badge" alt="Website"></a>
  <img src="https://img.shields.io/badge/Phases-34-60a5fa?style=for-the-badge" alt="34 phases">
  <img src="https://img.shields.io/badge/Tools-70-a78bfa?style=for-the-badge" alt="70 tools">
  <img src="https://img.shields.io/badge/Runs-in%20your%20browser-f59e0b?style=for-the-badge" alt="Runs in your browser">
  <img src="https://img.shields.io/badge/No%20server-no%20tracking-ef4444?style=for-the-badge" alt="No server">
</p>

<p align="center">
  <a href="#-why-webrecon">Why</a> ·
  <a href="#-key-features">Features</a> ·
  <a href="#-the-attack-surface-map">Map</a> ·
  <a href="#-the-phases">Phases</a> ·
  <a href="#-responsible-use">Responsible use</a> ·
  <a href="#-connect">Connect</a>
</p>

---

## ✨ Why WebRecon

Recon is where most bug bounty and pentest work begins, and it is easy to lose the thread: dozens of tools, hundreds of output files, and no clear answer to "what should I run next?"

WebRecon gives you a **methodology**, not a pile of commands.

> **One domain in → one ordered workflow out.** Every command is built for your target, every step tells you what good looks like, and nothing runs without you.

---

## 🚀 Key features

| | Feature | What it gives you |
|:-:|---|---|
| 🗺️ | **Visual attack-surface map** | A live tree of 95 steps. Horizontal and vertical tracks merge into one list. Click any step to see its purpose, inputs and outputs. |
| ⌘ | **Copy-ready commands** | Copy one command, a whole phase, or the full script (`.sh`) in one click. |
| 🎯 | **Expected results** | Every output file has a *good looks like*, an *if empty* and a *next step* note. |
| 🔎 | **Flag explanations** | The ⓘ icon next to a command explains each flag in plain language. |
| 🟢🔴 | **Recon vs. vulnerability cards** | Green for discovery, red for vulnerability checks, so you always know which phase you are in. |
| 📊 | **Segmented progress bar** | One segment per phase, filled as you go, with a glow when everything is done. |
| ✅ | **Checkboxes per domain** | Progress is saved in your browser for each target. |
| 💾 | **Save and open projects** | Export your domain, settings and progress as one JSON file. Auth headers are never saved. |
| 🧰 | **Tools and install guide** | Install commands, setup notes, API key guidance and a search box for all 70 tools. |
| 🔐 | **Authenticated testing** | Paste your own test-account header once, and logged-in crawling and checks use it. |
| 📱 | **Works on any screen** | Wide workflow on desktop, scaled map with a details panel on phones. |

---

## 📸 Screens

<p align="center">
  <img src="assets/hero.png" alt="Enter a domain and generate the workflow" width="32%">
  <img src="assets/command.png" alt="Copy-ready commands with flag help" width="32%">
  <img src="assets/tools.png" alt="Tools, install and setup notes" width="32%">
</p>

## 🗺️ WebRecon methodology

This is the real workflow from the site: 95 steps, drawn from the same data the tool uses.

<p align="center">
  <img src="assets/workflow-tree.png" alt="WebRecon methodology: workflow tree of 95 steps, recon in green, vulnerability checks in red" width="100%">
</p>


<details>
<summary><b>Show all 95 steps in a table</b></summary>

<sub>🔴 = vulnerability check.</sub>

<table>
<thead><tr><th>Step</th><th>Track</th><th>Name</th><th>Tool</th><th>Writes</th></tr></thead>
<tbody>
<tr><td rowspan="1" align="center"><b>0</b></td><td>Shared</td><td>Target scope and workspace</td><td><code>shell</code></td><td><code>~/recon/example.com/</code></td></tr>
<tr><td rowspan="6" align="center"><b>1</b></td><td>Vertical recon</td><td>Amass passive</td><td><code>amass</code></td><td><code>subs_amass.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Assetfinder</td><td><code>assetfinder</code></td><td><code>subs_assetfinder.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Certificate transparency</td><td><code>curl + jq</code></td><td><code>subs_crtsh.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Merge and clean passive subs</td><td><code>sort / grep</code></td><td><code>subdomains_passive.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Subfinder</td><td><code>subfinder</code></td><td><code>subs_subfinder.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Vertical recon start (subdomains and assets)</td><td><code>strategy</code></td><td>·</td></tr>
<tr><td rowspan="8" align="center"><b>2</b></td><td>Horizontal recon</td><td>ASN and CIDR ranges</td><td><code>asnmap</code></td><td><code>asn_cidrs.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Expand CIDR to IPs</td><td><code>mapcidr</code></td><td><code>ips_expanded.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Horizontal recon start (org, ASN, IP ranges)</td><td><code>strategy</code></td><td>·</td></tr>
<tr><td>Horizontal recon</td><td>In-scope acquisition hosts</td><td><code>grep / sort</code></td><td><code>acq_hosts.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Org name from WHOIS</td><td><code>whois</code></td><td>·</td></tr>
<tr><td>Horizontal recon</td><td>Port scan on ranges</td><td><code>naabu</code></td><td><code>range_ports.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Reverse DNS sweep (PTR)</td><td><code>dnsx</code></td><td><code>ptr_hosts.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>TLS SAN sweep</td><td><code>tlsx</code></td><td><code>tls_hosts.txt</code></td></tr>
<tr><td rowspan="4" align="center"><b>3</b></td><td>Horizontal recon</td><td>Merge candidate IPs</td><td><code>grep</code></td><td><code>origin_ips.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Origin IP sources</td><td><code>shodan / urlscan / OTX</code></td><td><code>origin_shodan.txt</code>, <code>origin_urlscan.txt</code></td></tr>
<tr><td>Horizontal recon</td><td>Verify origin (Host header + TLS)</td><td><code>curl / openssl</code></td><td>·</td></tr>
<tr><td>Horizontal recon</td><td>Virtual host fuzzing</td><td><code>ffuf</code></td><td><code>vhost results (json per IP)</code></td></tr>
<tr><td rowspan="3" align="center"><b>4</b></td><td>Vertical recon</td><td>DNS bruteforce</td><td><code>puredns</code></td><td><code>dns_brute.txt</code></td></tr>
<tr><td>Vertical recon</td><td>DNS permutations (alterx)</td><td><code>alterx</code></td><td><code>alterx_out.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Resolve permutations</td><td><code>puredns</code></td><td><code>perm_resolved.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>5</b></td><td>Shared</td><td>Final subdomain list (H + V merged)</td><td><code>sort</code></td><td><code>subdomains.txt</code></td></tr>
<tr><td rowspan="4" align="center"><b>6</b></td><td>Shared</td><td>Alive hosts</td><td><code>httpx</code></td><td><code>alive.txt</code></td></tr>
<tr><td>Shared</td><td>Favicon hashes</td><td><code>httpx</code></td><td><code>favicon_hashes.txt</code></td></tr>
<tr><td>Shared</td><td>Screenshots</td><td><code>gowitness</code></td><td><code>screenshots/</code></td></tr>
<tr><td>Shared</td><td>Status, title, tech</td><td><code>httpx</code></td><td><code>alive_details.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>7</b></td><td>Shared</td><td>WAF detection</td><td><code>wafw00f</code></td><td><code>waf_results.txt</code></td></tr>
<tr><td rowspan="8" align="center"><b>8</b></td><td>Shared</td><td>CMS detection (CMSeeK)</td><td><code>CMSeeK</code></td><td><code>CMSeeK results folder</code></td></tr>
<tr><td>Shared</td><td>Split hosts by CMS</td><td><code>grep</code></td><td><code>wp_hosts.txt</code>, <code>joomla_hosts.txt</code></td></tr>
<tr><td>Shared</td><td>Tech and CMS fingerprint</td><td><code>whatweb</code></td><td><code>whatweb_brief.txt</code></td></tr>
<tr><td>Shared</td><td>WordPress users (REST API)</td><td><code>curl + jq</code></td><td><code>wp_users.txt</code></td></tr>
<tr><td>Vulnerability</td><td>CMS templates (nuclei) 🔴</td><td><code>nuclei</code></td><td><code>cms_nuclei.txt</code></td></tr>
<tr><td>Vulnerability</td><td>Drupal scan 🔴</td><td><code>droopescan</code></td><td><code>droopescan_results.txt</code></td></tr>
<tr><td>Vulnerability</td><td>Joomla scan 🔴</td><td><code>joomscan</code></td><td><code>joomscan_results.txt</code></td></tr>
<tr><td>Vulnerability</td><td>WordPress scan (WPScan) 🔴</td><td><code>wpscan</code></td><td><code>wpscan_HOST.txt</code></td></tr>
<tr><td rowspan="3" align="center"><b>9</b></td><td>Shared</td><td>DNS records and CNAMEs</td><td><code>dnsx</code></td><td><code>dns_records.txt</code>, <code>cnames.txt</code></td></tr>
<tr><td>Vulnerability</td><td>Subdomain takeover (Subzy) 🔴</td><td><code>subzy</code></td><td>·</td></tr>
<tr><td>Vulnerability</td><td>Takeover templates 🔴</td><td><code>nuclei</code></td><td><code>takeover_nuclei.txt</code></td></tr>
<tr><td rowspan="2" align="center"><b>10</b></td><td>Shared</td><td>Detailed service scan</td><td><code>nmap</code></td><td><code>nmap_services.nmap</code></td></tr>
<tr><td>Shared</td><td>Port scan</td><td><code>naabu</code></td><td><code>ports.txt</code></td></tr>
<tr><td rowspan="5" align="center"><b>11</b></td><td>Shared</td><td>GAU archived URLs</td><td><code>gau</code></td><td><code>urls_gau.txt</code></td></tr>
<tr><td>Shared</td><td>Gospider crawl</td><td><code>gospider</code></td><td><code>urls_gospider.txt</code></td></tr>
<tr><td>Shared</td><td>Katana crawl</td><td><code>katana</code></td><td><code>urls_katana.txt</code></td></tr>
<tr><td>Shared</td><td>Merge and dedupe URLs</td><td><code>uro</code></td><td><code>allurls.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Wayback URLs</td><td><code>waybackurls</code></td><td><code>urls_wayback.txt</code></td></tr>
<tr><td rowspan="3" align="center"><b>12</b></td><td>Shared</td><td>404 interesting files</td><td><code>httpx</code></td><td><code>dead_files.txt</code></td></tr>
<tr><td>Shared</td><td>Sensitive extensions</td><td><code>grep</code></td><td><code>sensitive_ext.txt</code></td></tr>
<tr><td>Vertical recon</td><td>Wayback CDX dump</td><td><code>curl</code></td><td><code>cdx_urls.txt</code>, <code>cdx_sensitive.txt</code></td></tr>
<tr><td rowspan="7" align="center"><b>13</b></td><td>Shared</td><td>Clean endpoint list</td><td><code>sed / sort</code></td><td><code>endpoints.txt</code></td></tr>
<tr><td>Shared</td><td>Hidden parameter discovery</td><td><code>arjun</code></td><td><code>arjun_params.json</code>, <code>arjun_urls.txt</code></td></tr>
<tr><td>Shared</td><td>Hidden parameters (x8)</td><td><code>x8</code></td><td><code>x8_params.txt</code></td></tr>
<tr><td>Shared</td><td>Merge all parameter sources</td><td><code>uro / sort</code></td><td><code>param_merge.txt</code></td></tr>
<tr><td>Shared</td><td>Parameterized URLs</td><td><code>grep / uro</code></td><td><code>params.txt</code>, <code>param_templates.txt</code></td></tr>
<tr><td>Vertical recon</td><td>ParamSpider archived params</td><td><code>paramspider</code></td><td><code>paramspider.txt</code></td></tr>
<tr><td>Vulnerability</td><td>IDOR candidates and manual tests 🔴</td><td><code>grep + manual</code></td><td><code>idor_candidates.txt</code></td></tr>
<tr><td rowspan="2" align="center"><b>14</b></td><td>Shared</td><td>Endpoints from the spec</td><td><code>jq</code></td><td><code>endpoints_api.txt</code></td></tr>
<tr><td>Shared</td><td>Find OpenAPI or Swagger spec</td><td><code>curl</code></td><td><code>api_specs.txt</code></td></tr>
<tr><td rowspan="2" align="center"><b>15</b></td><td>Shared</td><td>Authenticated crawl</td><td><code>katana</code></td><td><code>urls_auth.txt</code></td></tr>
<tr><td>Shared</td><td>Authenticated fuzzing</td><td><code>ffuf</code></td><td><code>ffuf_auth.json</code></td></tr>
<tr><td rowspan="6" align="center"><b>16</b></td><td>Shared</td><td>Endpoints and secrets in JS</td><td><code>jsluice</code></td><td><code>jsluice_secrets.txt</code>, <code>jsluice_urls.txt</code></td></tr>
<tr><td>Shared</td><td>JS URL list</td><td><code>grep</code></td><td><code>js.txt</code></td></tr>
<tr><td>Shared</td><td>JS from HTML (subjs)</td><td><code>subjs</code></td><td><code>js.txt</code></td></tr>
<tr><td>Shared</td><td>Live JS files</td><td><code>httpx</code></td><td><code>js_live.txt</code></td></tr>
<tr><td>Shared</td><td>Secrets in JS</td><td><code>SecretFinder</code></td><td><code>secrets.txt</code></td></tr>
<tr><td>Vulnerability</td><td>Exposures in JS 🔴</td><td><code>nuclei</code></td><td><code>js_exposures.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>17</b></td><td>Shared</td><td>GitHub org secret scan</td><td><code>trufflehog</code></td><td><code>trufflehog_github.json</code></td></tr>
<tr><td rowspan="1" align="center"><b>18</b></td><td>Vulnerability</td><td>Exposures and misconfig 🔴</td><td><code>nuclei</code></td><td><code>exposures.txt</code>, <code>misconfig.txt</code></td></tr>
<tr><td rowspan="4" align="center"><b>19</b></td><td>Shared</td><td>API route discovery</td><td><code>kiterunner</code></td><td><code>api_routes.txt</code></td></tr>
<tr><td>Shared</td><td>Directory discovery</td><td><code>dirsearch</code></td><td><code>dirsearch_out.txt</code></td></tr>
<tr><td>Shared</td><td>GraphQL fingerprint</td><td><code>graphw00f</code></td><td><code>graphql_fingerprint.txt</code></td></tr>
<tr><td>Vertical recon</td><td>FFUF fuzzing</td><td><code>ffuf</code></td><td><code>ffuf_example.com.json</code></td></tr>
<tr><td rowspan="7" align="center"><b>20</b></td><td>Shared</td><td>gf pattern split</td><td><code>gf</code></td><td><code>xss_candidates.txt</code>, <code>sqli_candidates.txt</code></td></tr>
<tr><td>Vulnerability</td><td>CORS check 🔴</td><td><code>nuclei + corsy</code></td><td><code>cors_nuclei.txt</code></td></tr>
<tr><td>Vulnerability</td><td>CRLF check 🔴</td><td><code>nuclei</code></td><td><code>crlf_nuclei.txt</code></td></tr>
<tr><td>Vulnerability</td><td>LFI check 🔴</td><td><code>nuclei</code></td><td><code>lfi_nuclei.txt</code></td></tr>
<tr><td>Vulnerability</td><td>Open redirect check 🔴</td><td><code>httpx</code></td><td><code>open_redirect.txt</code></td></tr>
<tr><td>Vulnerability</td><td>SSRF check 🔴</td><td><code>nuclei</code></td><td><code>ssrf_nuclei.txt</code></td></tr>
<tr><td>Vulnerability</td><td>XSS candidates 🔴</td><td><code>dalfox</code></td><td><code>dalfox_xss.txt</code></td></tr>
<tr><td rowspan="4" align="center"><b>21</b></td><td>Vulnerability</td><td>Blind XSS payloads (bxss) 🔴</td><td><code>bxss</code></td><td>·</td></tr>
<tr><td>Vulnerability</td><td>XSS reflection check (Gxss) 🔴</td><td><code>Gxss</code></td><td><code>gxss_reflected.txt</code></td></tr>
<tr><td>Vulnerability</td><td>XSS reflection check (kxss) 🔴</td><td><code>kxss</code></td><td><code>kxss_reflected.txt</code></td></tr>
<tr><td>Vulnerability</td><td>XSS testing (XSStrike) 🔴</td><td><code>XSStrike</code></td><td>·</td></tr>
<tr><td rowspan="2" align="center"><b>22</b></td><td>Vulnerability</td><td>SQL injection detection (ghauri) 🔴</td><td><code>ghauri</code></td><td><code>ghauri_out/</code></td></tr>
<tr><td>Vulnerability</td><td>SQL injection detection (sqlmap) 🔴</td><td><code>sqlmap</code></td><td><code>sqlmap_out/</code></td></tr>
<tr><td rowspan="1" align="center"><b>23</b></td><td>Vulnerability</td><td>SSRF callback check (interactsh) 🔴</td><td><code>interactsh</code></td><td>·</td></tr>
<tr><td rowspan="1" align="center"><b>24</b></td><td>Vulnerability</td><td>Access control check (two accounts) 🔴</td><td><code>curl + Autorize</code></td><td><code>access_control_check.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>25</b></td><td>Vulnerability</td><td>Template injection check (nuclei) 🔴</td><td><code>nuclei</code></td><td><code>ssti_nuclei.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>26</b></td><td>Vulnerability</td><td>OS command injection (commix) 🔴</td><td><code>commix</code></td><td><code>commix_out/</code></td></tr>
<tr><td rowspan="1" align="center"><b>27</b></td><td>Vulnerability</td><td>XXE check (nuclei) 🔴</td><td><code>nuclei</code></td><td><code>xxe_nuclei.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>28</b></td><td>Vulnerability</td><td>JWT checks (jwt_tool) 🔴</td><td><code>jwt_tool</code></td><td>·</td></tr>
<tr><td rowspan="1" align="center"><b>29</b></td><td>Vulnerability</td><td>OAuth and redirect checks 🔴</td><td><code>nuclei</code></td><td><code>oauth_nuclei.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>30</b></td><td>Vulnerability</td><td>Path traversal check (nuclei) 🔴</td><td><code>nuclei</code></td><td><code>traversal_nuclei.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>31</b></td><td>Vulnerability</td><td>Cloud misconfig 🔴</td><td><code>nuclei / aws cli</code></td><td><code>cloud_nuclei.txt</code></td></tr>
<tr><td rowspan="1" align="center"><b>32</b></td><td>Shared</td><td>Manual checks (browser)</td><td><code>browser</code></td><td><code>your notes</code></td></tr>
</tbody>
</table>

</details>

---

## 🧭 The phases

| Track | Phases | What it finds |
|---|---|---|
| 🟢 **Discovery** | Setup → Final list → Live hosts | Subdomains, DNS, origin IPs, live hosts, WAF and CMS |
| 🟢 **Content** | URLs, sensitive files, parameters, API, auth, JavaScript, GitHub | Endpoints, hidden parameters, exposed files, secrets |
| 🔴 **Vulnerability checks** | Takeover, exposures, gf candidates, XSS, SQLi, SSRF, access control, SSTI, command injection, XXE, JWT, OAuth, traversal and upload | Candidates to test by hand, each with a proof step |
| ⚪ **Wrap-up** | Cloud misconfiguration, manual checks, summary | Buckets, browser checks, file counts |

Every phase has a short *why it matters*, *what you should get* and *run this after* note.

---

## 🛠️ Built with

Plain HTML, CSS and JavaScript in a single file. No build step, no framework, no backend, and no account. Your domains and progress stay in your browser.

---

## ⚠️ Responsible use

WebRecon only generates commands. Running them is your responsibility.

- Test only **in-scope** targets, systems you own, or targets you have **written permission** to test.
- Read the program **rules** first. Some forbid scanning or credential testing.
- Use **your own test accounts**. Never access or change another user's data.
- Never run **brute force**. Keep request rates low and stop if a service struggles.
- Report findings through the program's official channel.

---

## 🗓️ Roadmap

- [ ] Mark every command as tested against a lab target
- [ ] More vulnerability classes (request smuggling, prototype pollution)
- [ ] Markdown report draft from completed steps
- [ ] Shareable project links

---

## 🤝 Contributing

Ideas, corrections and new tools are welcome. For a wrong flag or command, a pull request with the tool version you tested is the most useful thing you can send.

---

## 🔗 Connect

[![GitHub](https://img.shields.io/badge/GitHub-0×mun1r-181717?style=for-the-badge&logo=github)](https://github.com/0xmun1r)
[![Facebook](https://img.shields.io/badge/Facebook-Page-blue?style=for-the-badge&logo=facebook)](https://facebook.com/0xmun1r)
[![Telegram](https://img.shields.io/badge/Telegram-Channel-2CA5E0?style=for-the-badge&logo=telegram)](https://t.me/AccessXConnectBot)
[![YouTube](https://img.shields.io/badge/YouTube-Channel-FF0000?style=for-the-badge&logo=youtube)](https://youtube.com/@0xmun1r?si=BQwwz7HA2YfqKvaF)

🌐 Website: [webrecon.xyz](https://webrecon.xyz)

---

## 📄 Disclaimer and licence

WebRecon is provided as is, without warranty. You are responsible for the commands you run and for having permission to test any target. Third-party tools are separate projects with their own licences.

Licence: **MIT**. See the [LICENSE](LICENSE) file.

<p align="center"><sub>Made for the hunters who like to know where they are going. 🕸️</sub></p>
