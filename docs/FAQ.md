# Frequently Asked Questions (FAQ)

**DeenShield - Your Digital Guardian**

---

## 📋 General Questions

### What is DeenShield?
DeenShield is a **privacy-first Islamic content filtering system** for Windows that helps Muslims and Muslim families maintain digital purity by blocking harmful content across browsers and applications. It combines a desktop guardian app with browser extensions to provide comprehensive protection.

### Who is DeenShield for?
- 👨‍👩‍👧‍👦 **Muslim families** seeking to protect children from inappropriate content
- 🧔 **Individuals** struggling with online temptations
- 🏫 **Islamic schools and madrasahs** needing institutional protection
- 🕌 **Mosques** providing computer access to community members
- 🤲 **Anyone** committed to lowering their gaze online

### Is DeenShield free?
**Yes!** DeenShield v0.1.0 is completely **free for personal use**. We believe digital purity should be accessible to all Muslims.

**Future plans:**
- Personal/family use: Always free (Insha'Allah)
- Schools/organizations: Paid licenses (to sustain development)
- Optional donations welcome (Sadaqah Jariyah)

### Is the source code open source?
**Not currently.** The source code is **proprietary** to prevent bad actors from:
- Creating bypass tools
- Removing protection features
- Distributing modified malicious versions

**However:**
- Security researchers can request audit access (NDA required)
- We may open-source parts in the future
- Transparency through independent security audits

---

## 🔒 Privacy & Security

### Does DeenShield collect my data?
**Absolutely NOT.** DeenShield has **zero data collection**:
- ❌ No browsing history
- ❌ No usage statistics
- ❌ No telemetry or analytics
- ❌ No personal information
- ❌ No communication with external servers

**Everything happens locally on your device.** See our [Privacy Policy](PRIVACY_POLICY.md) for details.

### How can I verify DeenShield's privacy claims?
1. **Network Monitoring:** Use Wireshark or Fiddler to inspect traffic (you'll see only `localhost:47147` communication)
2. **File System Audit:** All data stored in `%APPDATA%\DeenShield\` (local only)
3. **Security Audit:** Request source code access for review (email: security@alhaqdigital.com)

### Is my guardian password secure?
**Yes.** Guardian passwords are:
- ✅ **Hashed** using bcrypt (industry standard)
- ✅ **Encrypted** using Windows DPAPI (Data Protection API)
- ✅ **Never transmitted** (stays local)
- ✅ **Not recoverable** even by us (we don't have your data!)

⚠️ **Important:** If you forget your password in v0.1.0, you'll need to reinstall. Password recovery coming in v0.2.

### Can DeenShield be bypassed?
**Honest answer:** Yes, with enough technical skill and admin privileges.

**What DeenShield protects against:**
- ✅ Accidental access to inappropriate sites
- ✅ Impulsive browsing decisions
- ✅ Children's unrestricted internet use
- ✅ Social engineering and phishing

**What it doesn't protect against:**
- ❌ Advanced users with admin rights disabling it
- ❌ Alternative browsers without the extension
- ❌ Booting into Safe Mode
- ❌ Physical access to the computer

**Philosophy:** DeenShield is a tool to **help** those who want to protect themselves. It's not a prison, but a guardian. Combine it with:
- Islamic education about digital ethics
- Parental supervision
- Trust and open communication

---

## 💻 Technical Questions

### What operating systems are supported?
**Currently:**
- ✅ Windows 10 version 1809+ (64-bit)
- ✅ Windows 11 (all versions)

**Planned:**
- ⏳ macOS (v0.4, Q3 2026)
- ⏳ Linux (v0.5, Q4 2026)
- ⏳ Android (v0.3 beta, v1.0 stable)
- ⏳ iOS (v0.3 beta, v1.0 stable)

### Which browsers are supported?
**Currently:**
- ✅ Google Chrome (Manifest V3)
- ✅ Microsoft Edge (Manifest V3)
- ✅ Mozilla Firefox (Manifest V2)
- ✅ Brave (Chrome extension compatible)
- ✅ Opera (Chrome extension compatible)

**Not yet:**
- ❌ Safari (macOS version needed first)
- ❌ Internet Explorer (obsolete browser)

### How much disk space does DeenShield use?
- **Desktop App:** ~100-150 MB installed
- **Browser Extension:** ~8-10 MB per browser
- **Database/Settings:** <5 MB
- **Total:** ~150-200 MB

### Does DeenShield slow down my computer?
**No.** DeenShield is built with Flutter and optimized for performance:
- **RAM Usage:** ~150-250 MB (comparable to a browser tab)
- **CPU Usage:** <1% idle, ~5-10% during content analysis
- **Browser Impact:** Minimal (extension adds <50ms page load time)
- **Startup:** Auto-starts in background (no noticeable delay)

### Can I use DeenShield on a laptop?
**Yes!** DeenShield works on:
- Desktop computers
- Laptops
- Tablets with Windows (Surface, etc.)
- Any device running Windows 10/11 64-bit

---

## 🛡️ Features & Functionality

### What types of content does DeenShield block?
**Content Categories:**
- 🚫 **Adult/Pornographic content** (images, videos, sites)
- 🎰 **Gambling sites** (casinos, betting, lotteries)
- 🍺 **Alcohol & drug-related** content
- 💰 **Interest-based finance** (Riba/usury)
- 💕 **Dating websites** and apps
- 🔞 **Extreme violence** and gore
- 🎵 **Inappropriate music videos** (optional)
- 🗣️ **Hate speech** targeting Muslims

**How it works:**
- AI-powered content analysis (offline)
- URL blacklists (community-curated)
- Keyword detection (Arabic + English)
- Image analysis (detects inappropriate images)

### Can I whitelist specific websites?
**Yes!** In the desktop app:
1. Go to Settings → Content Filtering
2. Add URLs to "Allowed List"
3. These sites will never be blocked
4. Requires guardian password

**Use cases:**
- Educational sites with flagged keywords
- Medical/health information sites
- News sites with occasional false positives

### Can I temporarily disable DeenShield?
**Yes, with guardian password:**
1. Open DeenShield dashboard
2. Click "Pause Protection"
3. Enter guardian password
4. Choose duration (15 min, 1 hour, until restart)
5. Protection re-enables automatically

⚠️ **Note:** This is for legitimate needs (e.g., research, tech support), not to bypass protection.

### Does DeenShield block social media?
**Not by default.** Social media (Facebook, Twitter, Instagram, TikTok) are not blocked entirely, but:
- ✅ Inappropriate posts/ads within social media are filtered
- ✅ Private/direct messages are NOT monitored (privacy!)
- ✅ You can manually add social media to block list

**Planned feature (v0.3):** "Social Media Safe Mode"
- Enforce SafeSearch/Restricted Mode
- Block DMs from strangers
- Filter comments with inappropriate language

### Can I block specific applications?
**Yes!** DeenShield can block any Windows application:
1. Go to "Apps" tab in dashboard
2. Click "Add Application"
3. Browse to `.exe` file (e.g., `game.exe`, `app.exe`)
4. Click "Block Application"
5. Requires guardian password to unblock

**Common uses:**
- Block games during study hours
- Restrict messaging apps
- Prevent uninstalling DeenShield

---

## 🔧 Installation & Setup

### Why does Windows show a security warning?
The installer is **not yet code signed** (requires expensive certificate ~$200-500/year).

**Safe to ignore because:**
- File is clean (no malware)
- Downloaded from official GitHub releases
- Verified with VirusTotal (0 detections)
- Open to security audits

**Coming soon (v0.2):** Code signing certificate to remove warnings.

### Do I need administrator rights to install?
**Yes, for installation only.**

**After installation:**
- Normal users can run DeenShield
- Admin rights required only for:
  - Blocking applications
  - Changing protection settings
  - Uninstalling

### Can I install on multiple computers?
**Yes!** Install on as many personal computers as you like:
- ✅ Your desktop
- ✅ Your laptop
- ✅ Family computers
- ✅ All devices you own

**For organizations (schools, offices):**
- Contact us for multi-device licensing: business@alhaqdigital.com

### Where are settings stored?
**Local database:** `%APPDATA%\DeenShield\`

**What's stored:**
- Guardian password (encrypted)
- Block lists (apps and sites)
- User preferences (theme, language)
- Usage statistics (optional, local only)

**To reset:** Delete this folder (requires admin rights).

---

## 🤝 Support & Community

### I found a bug. How do I report it?
**GitHub Issues:** https://github.com/alhaqdigital/deenshield-releases/issues

**Include:**
- DeenShield version (v0.1.0)
- Windows version (e.g., Windows 11 22H2)
- Browser and version
- Steps to reproduce
- Screenshots (if applicable)

### Can I request a feature?
**Yes!** Feature requests welcome:
- 💬 **GitHub Discussions:** https://github.com/alhaqdigital/deenshield-releases/discussions
- 📧 **Email:** feedback@alhaqdigital.com

**We prioritize based on:**
- Community votes (upvotes)
- Islamic benefit (protects Ummah)
- Technical feasibility
- Available funding

### Is there a user community?
**Coming soon!**
- 💬 **Discord Server:** In development
- 📱 **WhatsApp/Telegram Groups:** Planned
- 🌐 **Forums:** On our website

**Current channels:**
- GitHub Discussions (technical)
- Email support (support@alhaqdigital.com)

### How can I contribute to DeenShield?
**Without coding:**
- 🤲 **Donate:** Support development (GitHub Sponsors, PayPal)
- 🗣️ **Spread the word:** Tell other Muslims about DeenShield
- 📝 **Translate:** Help localize to other languages
- 🧪 **Beta testing:** Test new features before release
- 📚 **Documentation:** Improve guides and FAQs

**With coding skills:**
- 🔧 We may accept contributions in the future (after v1.0)
- 🔍 Security audits (request access)

---

## 💰 Donations & Funding

### How is DeenShield funded?
**Current funding model:**
- 💚 **Donations:** GitHub Sponsors, PayPal, Ko-fi
- 🤲 **Sadaqah Jariyah:** Voluntary ongoing charity
- 🏢 **Enterprise Licenses:** Paid features for organizations (future)

**No ads, no data selling, no dark patterns.**

### Where do donations go?
**100% to development:**
- 👨‍💻 Developer salaries (fair wage for halal work)
- 🖥️ Infrastructure (servers, domains, certificates)
- 🧪 Testing devices (phones, tablets, computers)
- 📚 Islamic consultations (scholars for content guidelines)
- 🎨 Design and UX improvements

**Transparency:** Annual financial reports published (Insha'Allah).

### Is this Sadaqah Jariyah?
**Yes, Insha'Allah!** Supporting DeenShield is **continuous charity** because:
- Every person protected from sin = reward for you
- Ongoing benefit to the Ummah = ongoing reward
- Helping others lower their gaze = multiplied reward

> *"When a person dies, their deeds come to an end except for three: ongoing charity (Sadaqah Jariyah), knowledge that is benefited from, and a righteous child who prays for them."* - Prophet Muhammad ﷺ

### Can I sponsor a specific feature?
**Yes!** Large donors can:
- Request priority development of specific features
- Get naming recognition (if desired)
- Receive early access to beta versions
- Direct influence on roadmap

**Contact:** business@alhaqdigital.com

---

## 🕌 Islamic Questions

### Is DeenShield approved by Islamic scholars?
**Currently:** Informal approval from several local imams.

**Goal:** Formal endorsement from major Islamic organizations:
- Islamic Society of North America (ISNA)
- Council on American-Islamic Relations (CAIR)
- European Council for Fatwa and Research (ECFR)
- International Union of Muslim Scholars (IUMS)

**Process:** Underway for v1.0 certification.

### Does blocking content replace Islamic education?
**No!** DeenShield is a **tool**, not a substitute for:
- 📚 Islamic education about modesty and purity
- 👨‍👩‍👧‍👦 Parental supervision and guidance
- 🤲 Personal taqwa (God-consciousness)
- 💬 Open communication about online dangers

**Use DeenShield as part of a holistic approach to digital parenting.**

### Is it permissible to use monitoring software in Islam?
**Short answer:** Yes, for **protection** and **guardianship**, not **spying**.

**Islamic principles:**
- ✅ **Guardianship:** Parents are responsible for protecting children
- ✅ **Accountability:** We will be asked about our families
- ❌ **Suspicion:** Don't monitor without valid reason (Quran 49:12)
- ❌ **Privacy:** Respect personal boundaries

**DeenShield philosophy:**
- Focus on **blocking** harmful content (prevention)
- Minimal **monitoring** (only for parental dashboard)
- No **spying** on private communications
- Transparency with family about protection

**Consult your local scholar** for specific family situations.

### What Quranic verses guide DeenShield?
**Core principles:**

> *"Tell the believing men to lower their gaze and guard their private parts. That is purer for them. Indeed, Allah is Acquainted with what they do."* (Quran 24:30)

> *"O you who believe! Enter into Islam completely and do not follow the footsteps of Satan. Indeed, he is to you a clear enemy."* (Quran 2:208)

> *"Indeed, the hearing, the sight, and the heart - about all those [one] will be questioned."* (Quran 17:36)

**These verses inspire our mission:** Helping Muslims protect their gaze, heart, and mind in the digital age.

---

## 🔮 Future Plans

### When will mobile apps be released?
**Timeline:**
- **v0.3 (Q2 2026):** Android & iOS beta (TestFlight)
- **v1.0 (Q1 2027):** Stable release on Google Play & App Store

**Features:**
- Cross-device sync with desktop
- Mobile app filtering
- In-app browser with protection
- Parent monitoring from phone

### Will there be a macOS version?
**Yes!** Planned for **v0.4 (Q3 2026)**.

**Challenges:**
- macOS app blocking requires different approach
- Apple's strict sandboxing
- Need for native Swift development

### Can DeenShield integrate with parental control routers?
**Great idea!** Planned for **v0.5 (Q4 2026)**.

**Integration possibilities:**
- OpenDNS / Cloudflare Family
- Pi-hole (network-level blocking)
- TP-Link Deco (router parental controls)
- UniFi Dream Machine (Ubiquiti)

**Benefit:** Network-level + application-level protection (multi-layered).

### Will there be a web-based dashboard?
**Planned for v0.4 (Q3 2026).**

**Features:**
- Manage family devices remotely
- View usage reports from anywhere
- Push updated block lists instantly
- Monitor children's devices (with permission)

**Privacy:** Optional feature (self-hosted or cloud with end-to-end encryption).

---

## 📞 Contact & Support

### How do I get help?
**Support channels:**
- 📧 **Email:** support@alhaqdigital.com (Response within 48 hours)
- 💬 **GitHub Discussions:** Community-driven Q&A
- 🐛 **Bug Reports:** GitHub Issues
- 📖 **Documentation:** README.md, INSTALLATION_GUIDE.md

### Where can I follow updates?
- ⭐ **GitHub:** Star the repo for release notifications
- 🐦 **Twitter/X:** [@DeenShield](https://twitter.com/DeenShield) (coming soon)
- 📧 **Newsletter:** Monthly updates (opt-in, privacy-respecting)
- 💬 **Discord:** Community server (in development)

### Can I partner with DeenShield?
**We welcome partnerships:**
- 🏫 **Islamic schools:** Subsidized/free licensing
- 🕌 **Mosques:** Community awareness programs
- 📱 **Tech companies:** API integrations
- 💼 **NGOs:** Bulk licensing for beneficiaries

**Contact:** partnerships@alhaqdigital.com

---

## 🤲 Final Thoughts

### Isn't this restricting freedom?
**Perspective:** DeenShield is **voluntary**. You choose to install it because:
- You want to protect yourself
- You want to protect your family
- You want to fulfill your Islamic duty

**Freedom in Islam:**
- True freedom = freedom from slavery to desires
- Restriction of harm = liberation for the soul
- Taqwa (God-consciousness) brings peace

**No one is forced to use DeenShield.** It's a tool for those committed to digital purity.

### What if I relapse despite using DeenShield?
**Remember:**
- 🤲 **Allah is Most Merciful:** Repent sincerely (Tawbah)
- 🔄 **Keep trying:** Failing doesn't mean you're a failure
- 💪 **Seek help:** Speak to an imam, counselor, or trusted friend
- 📚 **Learn:** Understand triggers and develop coping strategies
- 🤝 **Support groups:** Join Muslim accountability communities

**DeenShield is a shield, not a cage.** It helps, but ultimate success requires:
- Sincere intention (Niyyah)
- Trust in Allah (Tawakkul)
- Consistent effort (Istiqamah)

> *"Indeed, Allah does not change the condition of a people until they change what is in themselves."* (Quran 13:11)

---

**May Allah (SWT) make DeenShield a means of protection and purity for you and your family. Ameen.**

**JazakAllahu Khair for your interest!**

---

**Last Updated:** November 9, 2025  
**FAQ Version:** 1.0

**Alhaq Digital Services (ADS)**  
*Serving the Muslim Community Through Technology*

**Have a question not answered here?**  
📧 Email: support@alhaqdigital.com  
💬 GitHub Discussions: https://github.com/alhaqdigital/deenshield-releases/discussions
