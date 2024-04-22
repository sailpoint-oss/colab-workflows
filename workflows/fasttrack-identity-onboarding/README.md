Fast Track Identity Onboarding

These workflows will help you fast track Identity onboarding in Identity Security Cloud.

Workflow 1 - FastTrackUserOnboarding.json
			 Sends a form (User Onboarding Form.json) to the manager to collect information and sends back email notification with response.
			 
Workflow 2 - UserOnboardingServiceNowRequests.json
			 Receives form submitted by manager and based on the repsonse, creates Service Now ticket
			 
Workflow 3 - UserOnboardingAssignRoles.json
			 Receives form submitted by manager and based on the repsonse, requests roles for the user.



For more details about this form and workflow please refer to the blog here:
https://developer.sailpoint.com/discuss/t/fast-track-identity-onboarding/50793

PS - To import the form into your tenant you may have to remove the image tags from it.