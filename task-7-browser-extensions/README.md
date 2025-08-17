# 🛡 Task 7: Identify and Remove Suspicious Browser Extensions

## 🎯 Objective
Review installed Chrome extensions, identify suspicious ones, and remove potential security risks to ensure safer browsing.

---

## 🛠 Tools Used
- **Google Chrome** (Extension Manager: `chrome://extensions/`)
- Manual inspection of extension permissions & developer details

---

## 🧪 Steps Performed
1. Opened **Extension Manager** via `chrome://extensions/`
2. Enabled **Developer Mode** to view extension IDs
3. Reviewed installed extensions by checking:
   - Name & developer
   - Permissions requested
   - Incognito access settings
4. Disabled suspicious extensions temporarily for testing
5. Removed unnecessary/untrusted extensions permanently
6. Restricted permissions for trusted ones (set to *On click* or *Specific sites*)
7. Verified **default search engine & homepage** settings

---

## 📊 Extension Review Results

| Extension Name  | ID / Developer     | Permissions Used                  | Action   | Reason |
|-----------------|--------------------|-----------------------------------|----------|--------|
| uBlock Origin   | cjpalhdlnbpafi...  | Block ads only                    | ✅ Kept   | Trusted, useful |
| Grammarly       | kbfnbcaeplbcio...  | Access on selected sites          | ✅ Kept   | Productivity tool |
| PDF Helper Pro  | xyz123abc          | Access to all sites & history     | ❌ Removed | Suspicious & unnecessary |
| Unknown AdBlock | abc987xyz          | Change search settings, all sites | ❌ Removed | Fake/duplicate adblock |

---

## ⚠️ Risks of Malicious Extensions
- Steal cookies or passwords
- Inject ads or malware into sites
- Track browsing activity and exfiltrate data
- Hijack homepage or search engine

---

## ✅ Outcome
By cleaning up browser extensions and restricting permissions, the browser is now more secure with fewer attack surfaces.

---

