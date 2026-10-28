# AdGuard Whitelist for Banking & Authenticator Apps

This repository contains a curated AdGuard-compatible allowlist for banking, fintech, and authenticator services that commonly break when overly aggressive ad-blocking or DNS filtering is enabled.

## Purpose

The goal is to prevent false positives where legitimate banking, authentication, and security traffic is blocked by AdGuard DNS or browser ad filters.

This is especially useful for:

- Canadian banking apps such as RBC, Scotiabank, Neo, and Koho
- Authenticator services such as Proton and Microsoft
- Payment and checkout infrastructure used by banking apps
- CDN, mobile app, API, and identity infrastructure required for secure access

## What this repo includes

- `allowed-list.txt` — the main AdGuard filter list with exception rules
- `README.md` — project overview and usage notes

## Why this matters

Some banking apps and authentication services rely on:

- API subdomains
- mobile push endpoints
- CDN and edge delivery networks
- identity/OAuth flows
- security and anti-fraud infrastructure

If these are blocked, users may experience:

- app login failures
- MFA or authenticator issues
- repeated notifications or device prompts
- broken banking pages or missing app features

## How to use it

Import `allowed-list.txt` into AdGuard Home, AdGuard for Android/iOS, or another AdGuard-compatible filter source.

Example:

```text
@@||rbc.com^
@@||*.rbc.com^
@@||api.rbc.com^
@@||online.rbc.com^
```

## Covered categories

The list includes entries for:

- RBC Royal Bank
- Neo Financial
- Scotiabank
- Koho
- Affirm
- Proton Authenticator
- Microsoft Authenticator / Identity
- Supporting CDN and cloud infrastructure

## Notes

This list is meant to be a practical allowlist for daily use and is continuously updated based on observed blocked domains.

It is not a replacement for official bank support guidance, and some edge cases may still require manual additions based on your device, region, or app version.

## License

This project is provided as-is for personal and local filtering use.
