# Administration module
The Administration module contains administration functionalities to manage local accounts and to see app statistics like runtime information, sessions and schedules events.

## Features and limitations
- Management of User Accounts
- Read-only overview of
  - all active sessions
  - all schedules events
  - all runtime instances
- Runtime statistics

## Dependencies
- Atlas_UI_Resources package
- Mendix SSO module

## Mendix SSO
If you want to use this module in combination with Mendix SSO, use the following steps:
- Import the 'MendixSSO' module from the Marketplace (https://marketplace.mendix.com/link/component/111349)
- Make sure to either exclude or delete the microflows in the 'MOVE_THIS' folder of the MendixSSO module.
- Include the microflows prefixed with 'MendixSSO_' in the 'Mendix SSO' folder of the Administration module.
- Configure the MendixSSO_AfterStartup microflow from the Administration module as the After startup microflow. If there is already an After startup microflow, do not replace it, but add the MendixSSO_AfterStartup microflow as a sub-microflow in the existing microflow.
- If you previously used the Mendix SSO in your application, use the 'MendixSSO_MigrateUsersToAccount' microflow to migrate users from the MendixSSOUser to the Administration.Account specialization. Please read the instructions in the microflow carefully before executing the migration.

## License
See included [LICENSE](LICENSE) file

## Mendix marketplace
https://marketplace.mendix.com/link/component/23513
