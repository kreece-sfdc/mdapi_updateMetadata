# SFDX  App

## Create Org and Deploy Repo

<code>sfdx force:org:create -f config/project-scratch-def.json -s -a ALIAS</code>

<code>sfdx force:package:install -i 04t0N0000012ufa</code>

<code>sfdx force:source:push</code>

<code>sfdx force:org:open</code>

## Amend Profile

Navigate to System Administrator Profile and Set Tab Visibility for Bob to be Default On and SAVE

Amend Record Types Assignment against Bob and Move Bob1 and Bob2 to the right selection and SAVE

## Deploy Metadata

Open SoapUI, create SOAP project with metadata.xml file and create a request with the content from updateMetadata.xml, grab access token from CLI when you performed Org open command, change Soap API url to domain of the org and added the session token to the content
- This assigns Bob1 Record Type with Layout v3 for the System Administrator.

Navigate to Bobs Tab and create a new Record
- Note: section title is 'Awesomeness Section v3'

Change SoapUI metadata from Layout v3 to Layout v2 and deploy.

Note: Page Layout Assignment for System Administrator depploys and shows Layout v2

Refresh the newly created 'Bob' record and note the section title remains 'Awesomeness Section v3'
