# Administration module
The Administration module contains administration functionalities to manage local accounts and to see app statistics like runtime information, sessions and schedules events.

## Instructions
Steps to set-up when using Mendix SSO:
- Make sure to either exclude or delete the microflows in the 'MOVE_THIS' folder in the MendixSSO module.
- Configure the MendixSSO_AfterStartup microflow from this module (Marketplace modules > Administration > Mendix SSO) as the After startup microflow. If there is already an After startup microflow, you should not replace it, but add the MendixSSO_AfterStartup microflow as an action in the existing microflow.

Steps to set-up without using Mendix SSO:
- Delete or exclude the microflows in the 'Mendix SSO' folder (Marketplace modules > Administration > Mendix SSO) if you do not want to make use of Mendix SSO.

## License
https://www.mendix.com/terms-of-use/

## Mendix marketplace
https://marketplace.mendix.com/link/component/23513
