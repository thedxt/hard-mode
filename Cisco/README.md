# Cisco
Commands for hardening Cisco devices

### Set Commands
- no cdp run
  - **Why**: "It is useful only in network monitoring and troubleshooting situations but is considered a security risk because of the amount of information provided from queries. In addition, there have been published denial-of-service (DoS) attacks that use CDP. CDP should be completely disabled unless necessary." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:d9c4272798759626cf0e055255b44e90)
- no ip source-route
  - **Why**: "Source routing is a feature of IP whereby individual packets can specify routes. This feature is used in several kinds of attacks." "Unless a network depends on source routing, it should be disabled." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.0_Level_1.audit:74f9137bdedf05647838896fe5ad05f8) and [Cisco](https://community.cisco.com/t5/other-security-subjects/what-is-ip-source-route/m-p/2516037/highlight/true#M141179)
