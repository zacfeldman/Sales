# The Demo

## Who are you meeting?



1. COO
2. CEO
3. Credit Vetting

{% hint style="info" %}
For both landlords and Property Management companies it is important to try meet with the COO and if possible the credit vetting or back office admin team. These are the people who understand the every day pain and the need for LeaseHub
{% endhint %}

## Start the Demo

Begin with the Landing page. Each element of the landing page can talk to a different need within a company.&#x20;

### Focus Area

The focus area is is used by management to identify key buildings that they want agents to focus on that month.

Landlords may not find this particularly useful and therefore the audience should be considered when spending time on this feature.&#x20;

![Landing Page](<.gitbook/assets/image (1) (1) (1).png>)

### Favorites

Favorites are used to mark items that are needed often that you are working on at the moment. These can be various documents depending on the users roles. Some examples of these are&#x20;

1. Leases
2. applications&#x20;
3. Proof of payments
4. contact sheets
5. TPN reports&#x20;

### Dashboard

The dashboards are configurable and can change as per the clients requirements. Any dashboard from the management dashboards  can be configured onto the landing page.&#x20;

{% hint style="success" %}
The dashboards are permission based and therefore  agents will only see the data that they can see whereas management will see the entire portfolio&#x20;
{% endhint %}

### My Tenant leases

This section is used to add all the leases for an agent that they can then use to track their current leases



## Start new application&#x20;

Applications can be started in 2 ways.

{% hint style="info" %}
If a prospective client already has an application process you can skip this part and move directly to the lease generation. there is no need to show this they already have a  process.
{% endhint %}

### Manual application

The most common way for an application to be started is by an agent. The agent will meet with the prospective tenant and start a new application once the applicant is ready to apply.

![](<.gitbook/assets/image (1) (1).png>)

### Applications from CRM

LeaseHub has a dedicated endpoint for starting applications that can intgrate into any CRM.

By using either [_Zapier_](https://zapier.com/app/dashboard) __ or other software agents can easily start new applications.&#x20;

{% swagger method="post" path="" baseUrl="https://property-dev.papertrail.co.za/management/api/generateApplication" summary="Create a new application" %}
{% swagger-description %}
This is used to start a new application
{% endswagger-description %}

{% swagger-parameter in="header" name="${APIKEY}" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    "status": "Success",
    "docId": 5379,
    "applicant_id": "000063",
    "application_id": "App000331"
}
```
{% endswagger-response %}
{% endswagger %}

## Application View

![Rent and Fees](<.gitbook/assets/image (2).png>)

The Rent and Fees section will auto calculate the first payment as well as the total monthly payment.

A discount field is also available for first month rental discounts

If these values are static per building we can build these to be automatically completed.

These fields can change slightly based on the needs of the client.&#x20;

### Volume based

Each companies workflow will differ slightly dependent on volumes. The more applications and leases they sign a month the more they will want their agents to do the majority of the work and limit the bottle neck at the credit vetting team

However, agents are more likely to make mistakes and therefore can only be used when the volume is large enough to justify a few errors.&#x20;

Unless the company is doing about 100 leases they won't want to take the risk of not having the back office or credit vetting checking all the documents.&#x20;

{% hint style="info" %}
Configure LeaseHub to mimic the process of the client you are showing the system to. Make sure that there is a back office user and credit vetting for small clients and show the responsibility of agents for large client.
{% endhint %}

## TPN

Send for credit check button will do an API call to TPN.

This call uses the TPN Credex module and will ask the user to select one of three options&#x20;

1. Credex basic&#x20;
2. Credex silver&#x20;
3. Credex Gold

All 3 options will return a report with the tenants TPN credit check.&#x20;

For Gold it will do an affordability check. It is important that the rental total is correct here as this will be sent to TPN for an assessment. For a client that uses gold it is important to show the assessment as well as the affordability rate.

## The deposit

Managing the receival of deposits is one of the most vital aspects of Leasehub. Most residential managing agents will not even generate a lease without a deposit being paid.&#x20;

Once the deposit is paid, the agent can then generate a lease.&#x20;

To capture a successful payment Leasehub has the following options. We send an email to the tenant with a link to upload the Proof of payment. This link **IS** mobile friendly and can be used to take a picture of atm deposit slip or upload the bank eft Proof of Payment.&#x20;

Alternately, the agent or the credit vetting team can upload the Proof of Payment on the tenants behalf.&#x20;

{% hint style="info" %}
Most managing agents do not want to do credit card or direct EFT as this will cut into their margins. However, if a landlord is managing their own portfolio they may require payment gateway integration to collect payments quicker.
{% endhint %}

Future development is being considered to integrate with payment gateways such as _Walletdoc_ that can accommodate both Direct EFT as well as Credit card payments.

If required; the full deposit amount must be captured prior to the lease being generated.&#x20;

## Proforma Invoice

