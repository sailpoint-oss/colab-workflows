**Configuration** 

Form
VS Code:

1. Navigate to the project directory, right-click on the 'forms' section, and select "import".
2. Choose the file you downloaded from this page, "Form - Delayed Birthright Role DeProvisioning.json".

Log in to the Environment and Update the Owner

Workflow
1. Open the file "Workflow - Delayed Birthright Role DeProvisioining on Transfer.json" and replace the tokens in the file.

URLs

- %%API_URL%% (e.g. https://company1983-poc.api.identitynow-demo.com)

Oauth Client Tokens

- %%OAUTH_CLIENT_ID%%

Admin Email (for emailing on failed provisioning events)

- %%ADMIN_EMAIL%%

Import

UI Option: Workflows > New Workflow > Upload File

VS Code option: In project directory, right click Workflows section and choose "import" and choose the file you just updated.

Update Client Secret

UI Option: Open Workflow > Edit in Builder > update client secret in the following steps:

1. Get Identity History Snapshots
2. Get Removed Roles
3. Make Role Requestable
4. Make Role Unrequestable

VS Code Option

Locate and replace “oAuthClientSecret” key occurrences (total of four times), inserting your client secret value accordingly. Note that this secret will not encrypt until you make modifications via UI & save.

Additional Details

- For more than one role, an access request would be created for each role.
- Typically, birthright roles are configured as non-requestable. This workflow loops through each role designated for an extension and modifies the role status to requestable. This temporarily allows for role assignment with an expiration date before immediately reverting the role back to being non-requestable, therefore securing system integrity.
