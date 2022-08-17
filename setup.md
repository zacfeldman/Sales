# Setup

## Requirements for new setup &#x20;



| Field                 | Description                                                                                                       | Comments                                                                                                                      |
| --------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| URL name              | Leasehub website                                                                                                  |                                                                                                                               |
| Email information     | The SMTP configuration                                                                                            | This is so that emails will go from the custom domain and not [noreply@egis-software.com](mailto:noreply@egis-software.com).  |
| Application form      |                                                                                                                   | This is used to see if any fields are missing on the LeaseHub application form                                                |
| Company info          | This is used for emails to client and leases - registration , email, tell number                                  |                                                                                                                               |
| TPN Integration       | API username and Password                                                                                         |                                                                                                                               |
| Groups and users      | gents names and emails, creditors names and emails, management names and emails                                   |                                                                                                                               |
| SMS configuration     | The mobile provider credentials username and password.                                                            |                                                                                                                               |
| Deposit calculation   | The deposit calculation fields from the application                                                               | Eg:  first month rent+ deposit + lease admin fee                                                                              |
| House rules           | PDF document of house rules.                                                                                      | These can be either per company or per building                                                                               |
| Contact Sheet         | PDF document of Contact Sheet                                                                                     | This is used the welcome email with useful contact information                                                                |
| Email wording         | <ol><li>Successful application</li><li>Declined application</li><li> Welcome pack post signing of lease</li></ol> |                                                                                                                               |
| Company Logo          | Png file                                                                                                          |                                                                                                                               |
| Auto Decline          | Rules for declining an application without credit vetting                                                         |                                                                                                                               |
| Application Documents | <ol><li>Mandatory </li><li>Non Mandatory </li><li>Documents needed if field is selected in application</li></ol>  | For point 3. if married then marriage certificate                                                                             |





&#x20;

## Lookups

Getting all the lookups is vital to a successful implementation. This data can be exported from MDA or other software. If there is no integration with these software it is imperative that this is kept up to date to ensure the that lease has the correct data is written onto the lease.&#x20;



| Lookup                                | Description                                                                                                                                                                     | Link                                                                                                                       |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| <p></p><p>Agent lookups </p>          | Lookup for agent details                                                                                                                                                        | [https://1drv.ms/x/s!Auz-BXHu5ydvgelxvwpjSOAxC6gkqQ?e=FFWP16](https://1drv.ms/x/s!Auz-BXHu5ydvgelxvwpjSOAxC6gkqQ?e=FFWP16) |
| <p></p><p>Landlord Lookups</p><p></p> | landlord details. required 1 per building.                                                                                                                                      | [https://1drv.ms/x/s!Auz-BXHu5ydvgelzmuomVOAZkWClgA?e=0mKy5B](https://1drv.ms/x/s!Auz-BXHu5ydvgelzmuomVOAZkWClgA?e=0mKy5B) |
| Building lookups                      | Building lookups for each building. In many companies each building will have its own bank account. therefore this needs to be locked down in terms of editing to avoid fraud.  | [https://1drv.ms/x/s!Auz-BXHu5ydvgel15xK3zJgc0ZnG0g?e=8rk1Xd](https://1drv.ms/x/s!Auz-BXHu5ydvgel15xK3zJgc0ZnG0g?e=8rk1Xd) |
|                                       |                                                                                                                                                                                 |                                                                                                                            |
