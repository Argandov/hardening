## Guidelines for Firefox hardening

Notes: This was originally intended as a quick personal benchmark, but decided to upload it in case it is useful for someone else. Go ahead with caution and do your research.

The results of this guidelines render only a casual-use Firefox configuration. If you have special privacy/anonimity needs, or are concerned about sofisticated attack vectors, then please do not use Firefox (Or use it with other privacy-enhancing services/softwares). Do your own modifications and research as needed.

The purpose of this setup is for Privacy and protection against tracking/fingerprinting and malicious sites. **Not Anonimity**.

## 1. Firefox profiles
**Firefox profile manager:** "Win+R > firefox.exe -P" (Windows) / "firefox -P" (Linux). 

**Location:**
- (Windows) C:\Users\<*username*>\AppData\Roaming\Mozilla\Firefox\Profiles\<*profile_name*>
- (Linux) /home/<*username*>/
  
**Custom, automatic profiles (Worth to check them out):**
- User.js (https://github.com/arkenfox/user.js).
  - Download user.js file & modify as needed. Examples: 
    - user_pref("intl.accept_languages", "en-US, en");
    - user_pref("app.update.auto", true);
  - Save file in a new profiling location > Open profile manager > Create new profile and add the recently created folder.

- Firefox Profilemaker (https://ffprofile.com) 
  - Guidance provided at "start" click.
  - Download profile. Apply to a new profile.
 ## 2. Manual Configuration
 
 **About:preferences**
Common privacy/security preferences:
- OCSP enabled
- Enable DNT (Do Not Track)
- Disable cookies/Fingerprinting
- Manage cookie storage (As needed)
- Block dangerous content
- SOCKSv5 / HTTP proxy if needed.
- Enable DoH (DNS over HTTPS); select a secure DNS server. *(Needs more testing)*

**About:config**

- (TLS minimum version) "security.tls.version.min" -> 3, 
- (See the full URL @ search bar) browser.urlbar.trimURLs -> true
- (Randomize http referer) network.http.referer.spoofSource -> true
- (Disable fonts) browser.display.use_document_fonts -> 0
- (Auto-update Firefox) extensions.update.autoUpdateDefault -> true/false
- (Fingerprinting) privacy.resistFingerprinting -> true
- 
- See **saved Certificate Authorities (CA)**: about:certificate


## 3. Addons:
- Certificate patrol (Current Cas)
- EFF's Privacy Badger
- Cookie quick manager
- Privacy Settings / Ublock Origin / uMatrix (Advanced)
- User-Agent Switcher (Check for the most common user-agent headers)
- CanvasBlocker

## 4. Browsers to use:
- https://duckduckgo.com/
- https://startpage.com/

## 5. Tools for testing browser's fingerprint, headers, DNS leaks, etc.
- https://ipleak.net/ (Good for DNS leaks and headers check)
- https://panopticlick.eff.org (Good general browser check analysis)
- https://browserleaks.com/ (Good for fingerprinting analysis)
- http://ip-check.info/ (more advanced browser check)

## See also:
- https://ssd.eff.org/en/module/understanding-and-circumventing-network-censorship
- https://anonymous-proxy-servers.net/en/jondofox.html


Sources: Nathan House (StationX), Electronic Frontier Foundation (EFF), Mozilla Foundation, JonDonym.
