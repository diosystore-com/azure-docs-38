---
title: Azure direct routing known limitations  - Azure Communication Services
description: Known limitations of direct routing in Azure Communication Services.
author: boris-bazilevskiy
manager: rcole
services: azure-communication-services

ms.author: bobazile
ms.date: 09/29/2022
ms.topic: conceptual
ms.service: azure-communication-services
ms.subservice: pstn
---

# Known limitations in Azure telephony

This article provides information about limitations and known issues related to telephony in Azure Communication Services.

## Azure Communication Services direct routing known limitations

- Anonymous calling isn't supported.
    - will be fixed in GA release
- Different set of Media Processors (MP) is used with different IP addresses. Currently [any Azure IP address](./direct-routing-infrastructure.md#media-traffic-ip-and-port-ranges) can be used for media connection between Azure MP and Session Border Controller (SBC).
    - will be fixed in GA release
- When you change direct routing configuration (add SBC, change Voice Route, etc.), wait approximately five minutes for changes to take effect.
- If you move SBC FQDN to another Communication resource, wait approximately an hour, or restart SBC to force configuration change. 
- Azure Communication Services SBC Fully Qualified Domain Name (FQDN) must be different from Teams Direct Routing SBC FQDN.
- One SBC FQDN can be connected to a single resource only. Unique SBC FQDNs are required for pairing to different resources.
- Wildcard SBC certificates require extra workaround. Contact Azure support for details.
    - will be fixed in GA release
- Media bypass/optimization isn't supported.
- No indication of SBC connection status/details in Azure portal.
    - will be fixed in GA release
- Azure Communication Services direct routing isn't available in Government Clouds.
- Multi-tenant trunks aren't supported.
- Location-based routing isn't supported.
- No quality dashboard is available for customers.
- Enhanced 911 isn't supported.
- PSTN numbers missing from Call Summary logs.

## Next steps

### Conceptual documentation

- [Phone number types in Azure Communication Services](./plan-solution.md)
- [Plan for Azure direct routing](./direct-routing-infrastructure.md)
- [Pair the Session Border Controller and configure voice routing](./direct-routing-provisioning.md)
- [Pricing](../pricing.md)

### Quickstarts

- [Outbound call to a phone number](../../quickstarts/telephony/pstn-call.md)