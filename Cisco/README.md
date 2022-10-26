# Cisco
Commands for hardening Cisco devices

### Set Commands
- no cdp run
  - **Why**: "It is useful only in network monitoring and troubleshooting situations but is considered a security risk because of the amount of information provided from queries. In addition, there have been published denial-of-service (DoS) attacks that use CDP. CDP should be completely disabled unless necessary." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:d9c4272798759626cf0e055255b44e90)
- no ip source-route
  - **Why**: "Source routing is a feature of IP whereby individual packets can specify routes. This feature is used in several kinds of attacks." "Unless a network depends on source routing, it should be disabled." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.0_Level_1.audit:74f9137bdedf05647838896fe5ad05f8) and [Cisco](https://community.cisco.com/t5/other-security-subjects/what-is-ip-source-route/m-p/2516037/highlight/true#M141179)
- no service pad
  - **Why**: Packet Assembler/Disassembler (PAD) is generally not needed and is on by default. [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_17_v1.0.0_Level_1.audit:c3028ffab360046a5ede5701b1be49a2)
- service password-encryption
  - **Why**: "Requires passwords to be encrypted in the configuration file to prevent unauthorized users from learning the passwords just by reading the configuration" [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:2859527ba892b41a2e996b6ecda2e992)
- crypto key generate rsa (2048)
    - **Why**: no RSA key pairs exist and is needed for SSH [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:8c4e4d6f775cec82aec93376bad6b6f3)
- ip ssh version 2
    - **Why**: due to the weakness of SSH Version 1 only version 2 should be used [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:c0f0e37b79daec5eec4c77c553d9b9cf)
- ip ssh time-out 60
    - **Why**: No SSH timeout is defined [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:93c4b34409ea22fa7ffc5e61f3a5fec5)
