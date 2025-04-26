# Splunk Login/Logout/Failed Login Event Monitoring

## Project Overview
This project demonstrates monitoring of user authentication events (login, logout, and failed login attempts) on a Windows host machine using Splunk.

## Tools Used
- Splunk Enterprise (free version)
- Windows 11
- Basic Splunk SPL (Search Processing Language)

## Methodology
- Captured Windows Event Logs using Splunk.
- Created custom searches for:
  - Successful Logins (EventCode: 4624)
  - Logouts (EventCode: 4634)
  - Failed Logins (EventCode: 4625)
- Analyzed event data for monitoring user activity.

## Key Queries

### Successful Login Events
```spl
index=main sourcetype="WinEventLog:Security" EventCode=4624
