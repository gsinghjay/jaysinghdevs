---
title: "Why I Update Inventory After Every Policy Update"
date: 2023-04-10
tags: macOS jamf mdm inventory policy
---

### Why I Update Inventory After Every Policy Update

Aside from the Jamf representative telling me it was best practice, I want to do a deep dive on why this is the case.

In a Jamf Pro environment, updating inventory after every policy update is considered a best practice for several reasons:

1. Accurate information: Updating the inventory ensures that the information in the Jamf Pro server is up-to-date, reflecting the most recent changes made by the executed policies. This helps administrators make better decisions based on accurate device and user data.
2. Reporting: Regular inventory updates after policy executions allow administrators to generate accurate reports on device configurations, application installations, and policy compliance. This enables better management of the devices and assessment of policy effectiveness.
3. Smart groups: Jamf Pro uses smart groups to dynamically organize devices based on inventory criteria. When the inventory is updated after a policy update, devices can be accurately assigned to the appropriate smart groups. This ensures that the correct policies, configurations, and applications are deployed to the right devices.
4. Troubleshooting: Regular inventory updates help administrators identify potential issues with policy executions more easily. If a policy fails to apply or encounters an error, the updated inventory will reflect the discrepancy, enabling quicker identification and resolution of the issue.
5. License and compliance management: Accurate and up-to-date inventory data is essential for managing software licenses and ensuring compliance with organizational policies and industry regulations.
6. Optimized policy execution: Inventory updates after policy changes allow for more efficient policy execution. With accurate inventory data, administrators can better target policies to specific devices or users, reducing the need for unnecessary policy executions.

In conclusion, updating inventory after every policy update in a Jamf Pro environment ensures that administrators have the most accurate and up-to-date information to manage devices effectively, troubleshoot issues, and maintain compliance.

[Source from Jamf Pro Documentation](https://learn.jamf.com/bundle/jamf-pro-documentation-current/page/Computer_Inventory_Information.html)

<insert picture of `Maintenance` under `Options`.
