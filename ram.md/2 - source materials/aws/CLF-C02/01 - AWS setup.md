23-04-2025 16:22:44

Status : #child 

Tags : [[AWS - Cloud Practitioner]]

## AWS account setup

- My Account -> AWS management console
	- root - using email 
	-  - account ID or account alias -  we should always use this account that we set up. 

> we don't usually use the root account except for very particular reasons such as, 

### IAM dashboard

Access management -> users -> create new user by clicking on the Add user button
1. Set user details
	- User details
		- User name - 
	- AWS access type
		- Access key - Programmatic access
		- Password - AWS management console
		- Console Password
			- Auto generated - requires to create new password at next sign-in
			- Custom Password
2. Set Permissions
	- Add to user group -> create group 
		- Group Name : Admin
		- Policy name : AdministrativeAccess/ PowerUserAccess
3. Add tags (Optional)
4. Review -> Create user
5. Download csv or copy, user - Access Key ID - Secret Access Key - Password - Email login instruction 

## AWS budget 

In case of any *overbilling* or anything, we can go to the AWS support center and then raise a support case.

- Billing alert
- Billing alarm
- Set budgets
- SNS - mail alert

**Turn on MFA** using any authenticator app.

# Digital Transformation

1. Innovation waves - phenomenon closely related connected to technology life cycles.
	1. The latest wave is Cloud Technology
	2. Common pattern of a wave change of supply and demand
2. Burning Platform 
	1. When a company abandons old technology for new technology 
	2. Uncertainty of success can be motivated by fear
3. [Digital Transformation checklist](https://aws.amazon.com/government-education/digital-transformation/?public-sector-resources-dt.sort-by=item.additionalFields.sortDate&public-sector-resources-dt.sort-order=desc) - refer the pdf
4. Evolution of computing - General Computing (ec2) -> GPU computing (AWS Inferentiare) -> Quantum Computing (AWS Bracket)
5. Amazon Bracket - free tier 1 hour of quantum circuit simulation for first 12 months

## References

[AWS - Budget methods](https://docs.aws.amazon.com/cost-management/latest/userguide/budget-methods.html)

