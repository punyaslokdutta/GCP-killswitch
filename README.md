# GCP-Killswitch (Could have saved 3k with this , when private api keys were exposed )
 Add a limit on billing costs for your GCP account
 


## Details from Google
https://cloud.google.com/billing/docs/how-to/notify



## Enable Budget Notifications

Navigate to Billing
Navigate to Budgets & alerts
CREATE BUDGET

## Listen to Notifications via Cloud Function
Create a cloud function with trigger type Pub/Sub
Use the "index.js" and "package.json" scripts.
Swap out your project ID in the index.js file.
This script disable billing on the project which will render the services no longer working and stop any incremental costs from accruing.



## Enable Cloud Billing API


## Service Account Upgrade
Provide Billing Administration access to the Cloud Function Service Account


## Publish Sub/Pub Message


```javascript
{
    "budgetDisplayName": "name-of-budget",
    "alertThresholdExceeded": 1.0,
    "costAmount": 100.01,
    "costIntervalStart": "2019-01-01T00:00:00Z",
    "budgetAmount": 100.00,
    "budgetAmountType": "SPECIFIED_AMOUNT",
    "currencyCode": "USD"
}
```

![Publish Test Message](https://raw.githubusercontent.com/tmoody/Google-Cloud-Platform-Killswitch/main/images/pub-sub-test-message.png)


## Validate that Billing is Disabled

![Disabled Billing](Google-Cloud-Platform-Killswitch/main/images/billing-disabled.png)

