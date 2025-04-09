# win-kernel-uaf-lab
PoC for a Windows kernel UAF in win32kfull.sys using GDI palette spraying. Demonstrates object grooming, UAF trigger, and exploit path toward arbitrary R/W. Includes notes on CFG bypass and SMEP evasion. For red team research only.
# Win Kernel UAF Lab

Proof-of-concept for a use-after-free vulnerability in win32kfull.sys via GDI object grooming.

## Summary

- **Trigger**: `NtUserCreateWindowEx` with crafted window class and menu
- **Grooming**: GDI palette spray to create predictable heap layout
- **Bug Class**: Use-After-Free via window destruction and reallocation
- **Exploit Path**: Object reuse + kernel pointer leak → arbitrary R/W
- **Next Step**: SMEP bypass using call gate or ROP

This repo contains a fake skeleton exploit and notes for educational purposes only.
