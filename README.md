# SFDX  App

Create org

<code>sfdx force:package:install -i 04t0N0000012ufa</code>

<code>sfdx force:source:push</code>

<code>sfdx force:user:password:generate</code>

deploy updateMetadata.xml (assigns layout v3)

Create a 'Bobs' record and there should be a UI section called Awesomeness Section v3.

Change updateMetadata.xml to Bob v2 layout and deploy

NOTE: Do Not Click Edit Assignments!

Page Layout Assignment will change in 'Page Layout Assignments' section but when the 'Bobs' UI is refreshed it will remain on v3.
