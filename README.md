Prevent User Deletion if Assigned to an Incident (ServiceNow)
📌 Project Overview

In an IT Service Management (ITSM) environment, users are often assigned to incidents for issue resolution and tracking.
However, the default system allows user deletion even if they are actively assigned to incidents. This can result in:

❌ Broken data references

❌ Loss of accountability

❌ Workflow disruption

This project introduces a safeguard mechanism in ServiceNow that prevents the deletion of a user unless all assigned incidents are either closed or reassigned.

🚀 Problem Statement

The absence of validation for user deletion in ServiceNow poses risks such as incomplete incident management and disrupted IT workflows.

Objective:
Prevent the deletion of users who are still actively assigned to incidents.

🛠️ Solution Approach

The solution was developed using Skill Wallet Project on ServiceNow, and it ensures data integrity by:

Checking Assigned Incidents

Before a user is deleted, the system checks if they are assigned to any active incidents.

Blocking Deletion

If incidents exist, the deletion is blocked, and a warning is displayed to the administrator.

Allowing Deletion Safely

Deletion proceeds only if the user has no active incidents assigned.

🔧 Implementation Details

Platform: ServiceNow

Configuration Used:

Business Rule (before delete) on User [sys_user] table

GlideRecord query to check incidents assigned to the user

Condition validation to restrict deletion

✅ Key Benefits

Prevents broken references in incidents

Ensures accountability for assigned tasks

Maintains workflow continuity

Improves data integrity in ServiceNow

🔮 Future Enhancements

Notification system to inform managers when a user slated for deletion still has assigned incidents

Automated reassignment of incidents before deletion

Reporting dashboard for pending user deletions

👤 Author

CHALLAPALLI SRI NIDHI

ServiceNow Developer
