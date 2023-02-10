# Code Scanning JavaScript Tutorial

Welcome to the Code Scanning JavaScript Tutorial! This tutorial will take you through how to set up GitHub Advanced Security: Code Scanning the Pull Request. We will introduce a vulnerability [CVE-2018-20835](https://github.com/advisories/GHSA-x2mc-8fgj-3wmr) (aka Zip Slip) in a Pull Request.

## Procedure

1. Duplicate this repository into your GitHub Organization
2. Enable GitHub Advanced Security 
3. Configure the CodeQL Code Scanning workflow
4. Complete a CodeQL scan for the main branch
5. Edit Line 264 of `index.js` and commit this to a new branch

OLD: `var srcpath = path.join(cwd, path.join('/', header.linkname))`
NEW: `var srcpath = path.resolve(cwd, header.linkname)`

6. Create a Pull Request to `main` from the new branch