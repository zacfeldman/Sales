# General Configuration

\===

\###Deployment Instructions:

Ensure All scripts created:

1.

* ApplicationApprovedEmail.groovy
* AssignApplication.groovy
* AssignSupportingDocsToUser.groovy
* AuditApplication.groovy
* autoDeclineApplication.groovy
* CalculateDeposit.groovy
* CongratulationsEmail.groovy
* CreateBuildingGroup.groovy
* CreateMissingDocs.groovy
* CreateTenantUser.groovy
* DeclineEmail.groovy
* EmailAgreement.groovy
* EmailApplication.groovy
* EmailLandlord.groovy
* EmailSupportingDocs.groovy
* FileAdditionalDocs.groovy
* GenerateContactSheet.groovy
* GenerateLease.groovy
* GenerateLeaseRenewal.groovy
* GenerateMafadiInvoice.groovy
* GenerateMDA.groovy
* GenerateSummary.groovy
* GetUserDetails.groovy
* InvoiceUploaded.groovy
* MDAIndexed.groovy
* MDAIndexedCompleteTask.groovy
* MergeHouseRules.groovy
* MissingDocsEmail.groovy
* NotifyCreditVetting.groovy
* ReminderMessage.groovy
* RenewalSchedule.groovy
* SendSmsNotifications.groovy
* SetLookupIndexes.groovy
* SkipAgent.groovy
* SMSCareTaker.groovy
* SubmitInvoice.groovy
* TenantSignedNotification.groovy
* TpnCreditCheck.groovy
* UpdateApplicantStatuses.groovy
* UpdateApplicationHistory.groovy
* UpdatePOP.groovy
* UpdateSummary.groovy
* UpdateTenantSignIndexes.groovy
* ValidateApplicantDocs.groovy

1. Ensure System/Templates created:

* Additional Clauses.html
* application\_approved\_layout.html
* approved\_email\_layoutNoLink.html
* approved\_email\_link\_layout.html
* credit\_vetting\_layout.html
* House Rules.pdf
* invoice\_layout.html
* Lease Agreement Landlord.html
* lease\_agreement\_layout.html
* lease\_application\_decline\_layout.html
* lease\_application\_layout.html
* missing\_docs\_layout.html
* payment\_reminder\_email\_layout.html
* signature\_reminder\_email\_layout.html
* SMSAgent.html
* SMSAgentDeclined.html
* SMSCaretaker.html
* SMSTenant.html
* SMSTenantDeclined.html
* supporting\_docs\_layout.html
* Tenant statement.pdf
* tenant\_signed\_layout.html
* Layouts -> layoutNoLink.html
* Layouts -> layout.html

3 - Set MetaModels

* node: Property Management/Lease Agreements > name: LeaseAgreement

node: Property Management/Lease Applications > name: Lease Application

* \*\* node: Property Management/Lease Applicants > name: Applicants
* node: Property Management/Supporting Documents > name: Supporting Documents
* node: System/Property Management/Lookups/Landlord > name: Landlord Lookup
* node: System/Property Management/Lookups/Agent > name: Agent Lookup
* node: Property Management/Supporting Documents/Summary sheet > name: Summary Sheet
* node: Property Management/Supporting Documents/Proof of Payment > name: Proof Of Payment
* node: System/Property Management/Lookups/Agent > name: Building Lookup
* node: Property Management/Supporting Documents/Contact Sheet ? Contact Sheet
* node: System/Property Management/Lookups/Company > name: Company Lookup
* node: Property Management/Supporting Documents/Inspection Form name: Forms
* node: Property Management/Supporting Documents/Key Release name: Forms
* node: Property Management/Supporting Documents/MDA name: MDA
* node: Property Management/Supporting Documents/TPN name: TPN
* name: House Rules

4 - set properties: Property Management ->

a) set companies list in Properties:

* Name: Company Names(Comma Separated)
* Example: Company A,Company B

b) Invoice Generation Auto number ID

* Create a new auto num
* set Id in this property

c) Summary Sheet Required

* Do you required a summary sheet to be sent on Lease Generation?

d) Skip Agent After Application Submitted

* Does the application need to go to the Agent to verify documents or can this stage be skipped?

f) Deposit Calculation Indexing (Comma Spearated)

* Does the application need to go to the Agent to verify documents or can this stage be skipped?

g) Children Occupants Max Age

* how old can a child input be on the application?

h) Full Deposit Required

* Is the full deposit required to generate the lease?

i) Manager To Begin Lease

* The "Management" group will be assigned the application for lease generation

j) Application Expenses(Parking,Security,Refuse)

* Include these expsenses in the application?

j) Send Upload Link with Approved Email

* Congratulations email to include link to upload invoice for tenant?

k) TPN Information

* Set password,login,security code and tpn url

1. Create a Contact Sheet For each company

Name: "${company\_name} Contact Sheet"template: Contact Sheet

### API Documentation:

Set API KEY in properties - egis -> Signature api key

1. Create Application

POST ${hostname}/property/management/api/generateApplication/${APIKEY}Content-Type: application/x-www-form-urlencodedAuthorization: Basic

Available Form Parameters: and rules

'application\_type' -> Personal or Business

'tenant\_name' -> Required

'tenant\_id\_number' -> Required

'tenant\_registration\_or\_id\_3' -> (Third Occupant)

'tenant\_registration\_or\_id\_2' -> (Second Occupant)

'tenant\_cell\_no''tenant\_cell\_no\_alt''agent\_name' -> Required Field

'lease\_occupation\_date''premises\_unit\_no''premises\_unit\_type''tenant\_occupation''tenant\_current\_employer''tenant\_employment\_period''tenant\_employer\_contact''tenant\_gross\_salary''tenant\_employer\_address''tenant\_monthly\_expenses ''lease\_fee'

'lease\_water\_premises''lease\_sewarage\_premises''lease\_electricity\_premises''lease\_rental\_premises''lease\_refuse\_premises''lease\_security\_premises''lease\_rental\_parking\_fee''lease\_total\_amount''lease\_deposit''joint\_application' -> Boolean(true or false)

'lease\_occupants\_children\_ages''lease\_no\_of\_occupants''lease\_no\_of\_occupants\_children''heard\_about''address''suburb''city''province''postal''tenant\_passport\_1''tenant\_email\_address''tenant\_nationality\_1''tenant\_1\_marriage\_type''tenant\_married''applicant\_smokes''applicant\_pets''tenant\_occupation\_2' -> (Joint applicant)'tenant\_cell\_no\_2' -> (Joint applicant)'tenant\_cell\_no\_alt\_2' -> (Joint applicant)'tenant\_salary\_payday''tenant\_monthly\_expenses\_2' -> (Joint applicant)'tenant\_email\_address\_2' -> (Joint applicant)'tenant\_id\_number\_2' -> (Joint applicant)'tenant\_2\_non\_sa''tenant\_self\_employed''tenant\_name\_2' -> (Joint applicant)'tenant\_current\_employer\_2' -> (Joint applicant)'tenant\_employment\_period\_2' -> (Joint applicant)'tenant\_1\_non\_sa''tenant\_employer\_contact\_2' -> (Joint applicant)'tenant\_gross\_salary\_2' -> (Joint applicant)'lease\_occupants\_children\_ages\_2' -> (Joint applicant)'lease\_no\_of\_occupants\_2' -> (Joint applicant)'deposit\_amount''lease\_no\_of\_occupants\_children\_2' -> (Joint applicant)
