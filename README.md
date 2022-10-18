# Administration module
This module contains administration functionalities to manage local accounts and to see app statistics like runtime information, sessions, and scheduled events.

## Features and limitations
- Management of User Accounts
- Read-only overview of
  - all active sessions
  - all schedules events
  - all runtime instances
- Runtime statistics

## Dependencies
- Atlas_Core package
- Mendix SSO module

## Mendix SSO
If you want to use this module in combination with Mendix SSO, use the following steps:
- Make sure that your project contains the MendixSSO module (v3.0.0 or higher). If you do not have the MendixSSO module in your project yet, import the module from the Marketplace (https://marketplace.mendix.com/link/component/111349)
- Configure the MendixSSO_AfterStartup microflow (available in the 'Mendix SSO' folder) from the Administration module as the After startup microflow. If there is already an After startup microflow, do not replace it, but add the MendixSSO_AfterStartup microflow as a sub-microflow in the existing microflow.
- If you previously used the Mendix SSO in your application and used MendixSSOUser as the user entity, please use the 'MendixSSO_MigrateUsersToAccount' microflow to migrate users from the MendixSSOUser to the Administration.Account specialization. Make sure to read the instructions in the microflow carefully before executing the migration.

If you do not want to make use of Mendix SSO in your project, use the following steps:
- Delete the 'Mendix SSO' folder in this module or exclude all its microflows.

## License
See included [LICENSE](LICENSE) file

## Mendix marketplace
https://marketplace.mendix.com/link/component/23513
