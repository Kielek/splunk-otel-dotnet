# Supported .NET frameworks

This document captures the current and planned .NET runtime support matrix for
AppDynamics, OpenTelemetry .NET Automatic Instrumentation, and the Splunk
Distribution of OpenTelemetry .NET.

Last reviewed: 2026-06-09.

## TLDR

This table lists versions that are supported by at least one product today, plus
.NET 11 because it is planned after GA. It excludes historical unsupported
versions.

| .NET framework name/version | AppDynamics support now | OpenTelemetry/Splunk support now | After .NET 11 GA, planned for 2026-11-10 | After .NET Framework 4.6.2 deprecation on 2027-01-12 |
| --- | --- | --- | --- | --- |
| .NET 11 | Not supported; preview | Not supported; preview | Supported | Supported |
| .NET 10 | Supported | Supported | Supported | Supported |
| .NET 9 | Supported | Supported | Not supported after Microsoft EOL, unless grace period is approved | Not supported |
| .NET 8 | Supported | Supported | Not supported after Microsoft EOL, unless grace period is approved | Not supported |
| .NET Framework 4.8.1 | Supported | Supported | Supported | Supported |
| .NET Framework 4.8 | Supported | Supported | Supported | Supported |
| .NET Framework 4.7.2 | Supported | Supported | Supported | Supported |
| .NET Framework 4.7.1 | Supported on supported parent OS | Supported on supported parent OS | Supported until 2027-01-12 under standard OS lifecycle | Not supported under standard OS lifecycle |
| .NET Framework 4.7 | Supported on supported parent OS | Supported on supported parent OS | Supported until 2027-01-12 under standard OS lifecycle | Not supported under standard OS lifecycle |
| .NET Framework 4.6.2 | Supported | Supported | Supported until 2027-01-12 | Not supported |
| .NET Framework 3.5 SP1 | Supported | Not supported | AppDynamics supported; OpenTelemetry/Splunk not supported | AppDynamics support TBD for alignment; OpenTelemetry/Splunk not supported |

*Grace period note: a 3-month grace period might be accepted, but the decision is
still waiting for feedback from other maintainers. A longer grace period is
unlikely.

## Summary

AppDynamics and the OpenTelemetry/Splunk distribution are currently aligned for
modern .NET and .NET Framework 4.x:

- .NET 8, .NET 9, and .NET 10 are supported.
- .NET Framework 4.6.2 and later are supported.
- AppDynamics also supports .NET Framework 3.5. OpenTelemetry .NET and the
  Splunk distribution do not.

The desired long-term state is to fully align these support sets and follow
Microsoft-supported runtimes unless a short, explicit grace period is approved
and announced.

## Current support matrix

The AppDynamics column reflects the current AppDynamics support state provided
for this planning note. The OpenTelemetry/Splunk column follows the
OpenTelemetry .NET policy of supporting officially supported .NET versions,
except .NET Framework 3.5, and the OpenTelemetry .NET Automatic Instrumentation
minimum .NET Framework version of 4.6.2.

### Modern .NET

| Runtime | Microsoft status on 2026-06-09 | Microsoft end of support | AppDynamics | OpenTelemetry/Splunk distribution | OTel Auto release support | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| .NET 11 | Preview | TBD | Planned after GA | Planned after GA | Not yet supported | Preview release |
| .NET 10 | Supported, LTS, active | 2028-11-14 | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Current LTS baseline after .NET 8 reaches EOL. |
| .NET 9 | Supported, STS, maintenance | 2026-11-10 | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Planned removal candidate after Microsoft EOL, subject to grace-period decision. |
| .NET 8 | Supported, LTS, maintenance | 2026-11-10 | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Planned removal candidate after Microsoft EOL, subject to grace-period decision. |
| .NET 7 | Out of support | 2024-05-14 | Not supported | Not supported | Last supported by [v1.9.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.9.0), released 2024-11-06; support removed in [v1.10.0-beta.1](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.10.0-beta.1), released 2024-12-13 | Historical entry. |
| .NET 6 | Out of support | 2024-11-12 | Not supported | Not supported | Last supported by [v1.9.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.9.0), released 2024-11-06; support removed in [v1.10.0-beta.1](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.10.0-beta.1), released 2024-12-13 | Historical entry. |
| .NET 5 | Out of support | 2022-05-10 | Not supported | Not supported | Supported in the initial [v0.1.0-beta.1](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v0.1.0-beta.1), released 2022-04-22; support removed after .NET 5 EOL | Historical entry. |
| .NET Core 3.1 | Out of support | 2022-12-13 | Not supported | Not supported | Last supported by [v0.4.0-beta.1](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v0.4.0-beta.1), released 2022-10-27; support removed in [v0.5.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v0.5.0), released 2022-11-24 | Historical entry. |
| .NET Core 3.0 | Out of support | 2020-03-03 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |
| .NET Core 2.2 | Out of support | 2019-12-23 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |
| .NET Core 2.1 | Out of support | 2021-08-21 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |
| .NET Core 2.0 | Out of support | 2018-10-01 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |
| .NET Core 1.1 | Out of support | 2019-06-27 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |
| .NET Core 1.0 | Out of support | 2019-06-27 | Not supported | Not supported | No OTel Auto support identified | Historical entry. |

### .NET Framework

| Runtime | Microsoft status on 2026-06-09 | Microsoft end of support | AppDynamics | OpenTelemetry/Splunk distribution | OTel Auto release support | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| .NET Framework 4.8.1 | Supported, active | Not announced | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Latest .NET Framework version. Supported while installed on a supported Windows version. |
| .NET Framework 4.8 | Supported, active | Not announced | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Supported while installed on a supported Windows version. |
| .NET Framework 4.7.2 | Supported, active | Not announced | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Supported while installed on a supported Windows version. |
| .NET Framework 4.7.1 | Supported as Windows component | Parent OS lifecycle; effectively 2027-01-12 for standard support | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Microsoft does not list a standalone EOL date for 4.7.1, but the supported parent OS list tops out at Windows Server 2016 for normal long-term support. |
| .NET Framework 4.7 | Supported as Windows component | Parent OS lifecycle; effectively 2027-01-12 for standard support | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Microsoft does not list a standalone EOL date for 4.7, but the supported parent OS list tops out at Windows Server 2016 for normal long-term support. |
| .NET Framework 4.6.2 | Supported, active | 2027-01-12 | Supported | Supported | [v1.15.0](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases/tag/v1.15.0), released 2026-04-23 | Removal candidate after Microsoft EOL. |
| .NET Framework 3.5 SP1 | Supported, active | 2029-01-09 | Supported | Not supported | Not supported | Microsoft supports the runtime, but not developing new apps that target 3.5. This is the main current AppDynamics versus OTel/Splunk difference. |
| .NET Framework 4.6.1 | Out of support | 2022-04-26 | Not supported | Not supported | Historical entry. |
| .NET Framework 4.6 | Out of support | 2022-04-26 | Not supported | Not supported | Historical entry. |
| .NET Framework 4.5.2 | Out of support | 2022-04-26 | Not supported | Not supported | Historical entry. |
| .NET Framework 4.5.1 | Out of support | 2016-01-12 | Not supported | Not supported | Historical entry. |
| .NET Framework 4.5 | Out of support | 2016-01-12 | Not supported | Not supported | Historical entry. |
| .NET Framework 4.0 | Out of support | 2016-01-12 | Not supported | Not supported | Historical entry. |
| .NET Framework 3.0 | Out of support | 2011-07-12 | Not supported | Not supported | Historical entry. |
| .NET Framework 2.0 | Out of support | 2011-07-12 | Not supported | Not supported | Historical entry. |

## Planned changes

### November 2026 modern .NET transition

Microsoft support for .NET 8 and .NET 9 ends on 2026-11-10. The baseline plan is:

- Add .NET 11 support after .NET 11 reaches GA.
- Remove .NET 8 and .NET 9 support after Microsoft EOL.
- Keep .NET 10 support. .NET 10 is LTS and is supported by Microsoft until
  2028-11-14.

If support is removed on 2026-11-10, the 3-month legal notice deadline is
2026-08-10.

The OpenTelemetry .NET maintainer discussion has not reached final consensus.
The active options discussed are:

- Drop EOL runtimes at Microsoft EOL.
- Allow a short grace period, with 3 months as the preferred upper bound from
  the discussion so far. That would move .NET 8 and .NET 9 removal to
  2027-02-10, with a 2026-11-10 notice deadline for AppDynamics if that date is
  selected.
- During any grace period, limit work to critical/security fixes only.

### January 2027 .NET Framework 4.6.2 transition

Microsoft support for .NET Framework 4.6.2 ends on 2027-01-12. If support is
removed on that date, the 3-month legal notice deadline is 2026-10-12.

Important clarification: current Microsoft lifecycle product pages do not show
standalone EOL dates for .NET Framework 4.7 or 4.7.1. However, the .NET
Framework FAQ says .NET Framework 4.x follows the lifecycle of the parent
Windows OS on which it is installed. The FAQ-supported OS lists for
.NET Framework 4.7 and 4.7.1 top out at Windows Server 2016 for normal
long-term support, and Windows Server 2016 extended support ends on 2027-01-12.
Therefore, .NET Framework 4.7 and 4.7.1 should also be treated as unsupported
under the standard Microsoft lifecycle after 2027-01-12.

Extended Security Updates for Windows Server 2016 may provide a paid transition
path for the parent OS after 2027-01-12, but that should not be treated as the
baseline product support policy for AppDynamics or the Splunk distribution.

## Current discussion notes

The OTel .NET maintainer discussion raised these constraints:

- Customers often continue running EOL runtimes after Microsoft support ends.
- Continuing to build and test against EOL runtimes increases engineering cost,
  CI matrix size, conditional code, and backport complexity.
- Continuing to support EOL runtimes can require old build tooling or
  dependencies, which may itself create security risk.
- A short grace period can help customers through end-of-year deployment freezes,
  but a long grace period risks normalizing unsupported runtime usage.
- Security-only backports should be tightly bounded, for example to
  latest-minus-2 supported release lines, if that policy is adopted.
- Ubuntu/Canonical packages can extend runtime availability for specific Ubuntu
  releases, but that does not automatically solve unsupported dependency,
  tooling, or upstream package vulnerability questions.

Recommended policy direction for AppDynamics and the Splunk distribution:

- Announce removals at least 3 months before the effective date.
- Align support with Microsoft-supported runtimes by default.
- If a grace period is approved, keep it short and explicitly scope it to
  critical/security fixes.
- Make the support meaning explicit: "the runtime can be instrumented" is not
  the same as "all features, dependencies, and backports are fully supported."
- Resolve the .NET Framework 3.5 difference as part of the long-term AppDynamics
  and OpenTelemetry/Splunk alignment plan.

## References

- [.NET downloads](https://dotnet.microsoft.com/en-us/download/dotnet)
- [.NET and .NET Core support policy](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-core)
- [Microsoft .NET and .NET Core lifecycle](https://learn.microsoft.com/en-us/lifecycle/products/microsoft-net-and-net-core)
- [.NET Framework support policy](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-framework)
- [Microsoft .NET Framework lifecycle](https://learn.microsoft.com/en-us/lifecycle/products/microsoft-net-framework)
- [Install .NET Framework on Windows](https://learn.microsoft.com/en-us/dotnet/framework/install/on-windows-and-server)
- [OpenTelemetry .NET supported versions](https://github.com/open-telemetry/opentelemetry-dotnet#supported-net-versions)
- [OpenTelemetry .NET Automatic Instrumentation releases](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/releases)
- [OpenTelemetry .NET Automatic Instrumentation v0.1.0-beta.1 project file](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/blob/v0.1.0-beta.1/src/OpenTelemetry.AutoInstrumentation/OpenTelemetry.AutoInstrumentation.csproj)
- [OpenTelemetry .NET Automatic Instrumentation 0.5.x compatibility note](https://gitea.cncfstack.com/open-telemetry/opentelemetry-dotnet-instrumentation/src/commit/345beca02a83639c82487828eec59c8100c9afdf/docs/README.md)
- [OpenTelemetry .NET zero-code instrumentation compatibility](https://opentelemetry.io/docs/zero-code/dotnet/#compatibility)
- [OpenTelemetry .NET support policy discussion](https://github.com/open-telemetry/opentelemetry-dotnet/issues/7294)
- [.NET and Ubuntu overview](https://learn.microsoft.com/en-us/dotnet/core/install/linux-ubuntu-decision)
