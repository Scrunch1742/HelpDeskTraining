# Helpdesk Printer Troubleshooting Guide

This guide is designed for helpdesk technicians to walk end-users through printer troubleshooting step-by-step. It covers basic checks, OS/network troubleshooting, advanced steps, and escalation criteria.

---

## 1. Greeting & Quick Context
- "Hi — this is [Your Name] from Helpdesk. I’ll walk you through some quick checks to get your printer working. I’ll tell you exactly what to do; feel free to tell me what you see as we go."

---

## 2. Quick Questions to Ask
- "What’s the model/name on the printer display?"
- "Is there an error message or flashing light? If so, what does it say/what color is it?"
- "Can other people print to the same printer, or is it just you?"
- "Are you printing from a computer connected by USB or from the network (Wi-Fi/ethernet)?"

---

## 3. Reassure & Set Expectations
- "I’ll try the fastest fixes first (power cycle, clear queue). If none work I’ll escalate and document everything. If I need you to press anything I’ll tell you exactly which button."

---

## Level 1 — Quick Physical & User Checks (0–5 min)
- **Confirm the obvious:** Power on, error lights, paper in tray, toner/ink level.
- **Look for physical problems:** Paper jams, low toner, misfeeds, torn paper.
- **Connection check:** USB cables, network cables, Wi-Fi connectivity.
- **Power cycle:** Turn printer off, unplug 10–30s, power on again.

---

## Level 2 — OS/Queue & Basic Network Checks (5–15 min)
1. Try a simple test print from the user’s computer.
2. Check print queue:
   - **Windows:** Settings → Printers & scanners → select printer → Open queue
   - If jobs are stuck, cancel all and try printing again.
3. Restart Windows Print Spooler:
```cmd
net stop spooler
del /Q %windir%\System32\spool\PRINTERS\*.*
net start spooler
