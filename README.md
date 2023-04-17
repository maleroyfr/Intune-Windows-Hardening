# Intune Windows Hardening

These Microsoft Intune policies were put together to help organisations comply with the CIS Windows 11 Hardening Guidance.
This repository will provide exports of Intune policies that organisations will be able to import into their Intune tenant for deployment to their Windows devices.

Additional Intune policies will be provided in the future for other products like Microsoft Edge or Microsoft 365 Apps.

While the intent of these policies is to assist in an organisations compliance efforts, total compliance with CIS guidance is not guaranteed.

## What's included?
Currently supporting only Windows 11 
* There are three (3) Windows hardening policies based on the CIS Benchmark and one (1) Security Baseline for Windows 10 and later recreated with the Settings Catalog.

These Microsoft Intune policies are currently based on "**CIS Microsoft Intune for Windows 11 Benchmark version v1.0.0 - 01-26-202**"

To make things a little easier to navigate the repo has been split up into sections:


```
   |-CIS Microsoft Intune for Windows 11
   |-Security Baseline for Windows 10 and later
```

## Requirements

These policies were developed on Azure AD Joined Windows 10 & Windows 11 devices and can be deployed to either Operating System where Intune is providing the device configuration workload, regardless of join type.  Ensure that devices are [currently supported](https://docs.microsoft.com/en-us/windows/release-health/supported-versions-windows-client) and the appropriate Microsoft Endpoint Manager licences have been assigned.

Ensure that [KB5005565](https://support.microsoft.com/en-us/topic/september-14-2021-kb5005565-os-builds-19041-1237-19042-1237-and-19043-1237-292cf8ed-f97b-4cd8-9883-32b71e3e6b44) has been installed, which was released as a part of the September 14th, 2021 quality updates. This KB contains updated [Mobile Device Management](https://techcommunity.microsoft.com/t5/intune-customer-success/the-latest-in-group-policy-settings-parity-in-mobile-device/ba-p/2269167) policies. Without this update, the policies provided will not be applied successfully.

## How to import the policies

To import the policies, use [Graph Explorer](https://aka.ms/ge).
After running through the import instructions below, the following policies and profiles will be imported into the organisations Intune tenant. 
>Note: After importing the policies, the policies will need to be assigned to a group.
1. A Settings Catalog policy, named: XX Windows Hardening Guidelines*
2. A Security Baseline, named: XX Windows Security Baseline (for use with ACSC Windows Hardening Guidelines)*
3. An Attack surface reduction policy, named: XXX-Attack Surface Reduction*
4. A Custom configuration profile, named: *ACSC Windows Hardening Guidelines-User Rights Assignment*

>Note: When using Graph Explorer, you may need to consent to permissions if you have not done so before. For more information, please see [Working with Graph Explorer](https://docs.microsoft.com/en-us/graph/graph-explorer/graph-explorer-features).
