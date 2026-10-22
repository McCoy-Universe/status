# McCoy Status

Live status page: **https://status.mccoy.org**

## [📈 Live Status](https://status.mccoy.org): <!--live status--> **🟩 All systems operational**

<!--start: status pages-->
<!--end: status pages-->

## Posting an incident

Any unplanned outage lasting more than 60 minutes must be posted here, with updates until resolved.

- **Automatic:** when a check fails, an issue titled "🛑 <Component> is down" opens. Rename it to a customer-readable title, then post updates as comments (start each with **Investigating**, **Identified** or **Monitoring**). It closes itself when the check passes; add a final **Resolved** comment.
- **Manual** (checks green but users affected): open an issue, add the labels `status` and one of `learner-app`, `admin-console`, `api`, `sign-in`, post updates as comments, and close it after a **Resolved** comment.
- **Scheduled maintenance:** open an issue labelled `maintenance` whose body contains:

  ```
  <!--
  start: 2026-11-01T02:00:00Z
  end: 2026-11-01T03:00:00Z
  expectedDown: learner-app, api
  -->
  ```

Describe customer impact only — no internal service names, hosts, vendors or customer names.

Components are configured in [`.upptimerc.yml`](./.upptimerc.yml). Powered by [Upptime](https://upptime.js.org) (MIT).
