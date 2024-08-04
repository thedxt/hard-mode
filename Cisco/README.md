# Cisco
Commands for hardening Cisco devices

### Set Commands
- no cdp run
  - **Why**: "It is useful only in network monitoring and troubleshooting situations but is considered a security risk because of the amount of information provided from queries. In addition, there have been published denial-of-service (DoS) attacks that use CDP. CDP should be completely disabled unless necessary." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:86c2b9f7c174418fcbf6394f78fbb9bc)
- no ip source-route
  - **Why**: "Source routing is a feature of IP whereby individual packets can specify routes. This feature is used in several kinds of attacks." "Unless a network depends on source routing, it should be disabled." From [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:927dc23e4920340e6dbef59930843715) and [Cisco](https://community.cisco.com/t5/other-security-subjects/what-is-ip-source-route/m-p/2516037)
- no service pad
  - **Why**: Packet Assembler/Disassembler (PAD) is generally not needed and is on by default. [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_XE_17.x_v2.1.0_L1.audit:ed28812985a868a3a6faee241c3d1f6b)
- service password-encryption
  - **Why**: "Requires passwords to be encrypted in the configuration file to prevent unauthorized users from learning the passwords just by reading the configuration" [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:4f6d49a29f394145e7cbe53508685f31)
- crypto key generate rsa (2048)
    - **Why**: no RSA key pairs exist and is needed for SSH [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:82b17ae4b847be02ae9e391bd87eba50)
- ip ssh version 2
    - **Why**: due to the weakness of SSH Version 1 only version 2 should be used [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:f27c845b1db2481fb5742c1ab3eecca6)
- ip ssh time-out 60
    - **Why**: No SSH timeout is defined [Tenable](https://www.tenable.com/audits/items/CIS_Cisco_IOS_15_v4.1.1_Level_1.audit:aebe006f58b260b1123157ca557141e1)
