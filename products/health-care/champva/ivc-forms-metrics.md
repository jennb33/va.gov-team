# IVC Forms Metrics
| Metric/event               | Description                                                  | Event measured                | Source of truth  |
|----------------------------|--------------------------------------------------------------|-------------------------------|------------------|
| Submit                     | This represents the user clicking the submit button. It includes the form submitted and any supporting documents. | Forms library submission      | Google Analytics |
| Upload                     | This event represents our attempt to send a file to the s3 bucket. There is an upload event for each file included in a submit. | Upload controller             | [Datadog](https://vagov.ddog-gov.com/dashboard/zsa-453-at7/ivc-champva-forms)          |
| Upload error               | Upload errors represent each non-200 response to an upload attempt that is received from s3. | Upload controller             | [Datadog](https://vagov.ddog-gov.com/dashboard/zsa-453-at7/ivc-champva-forms)          |
| Status update              | For every upload, there should be a corresponding status update from PEGA. | PEGA callbacks                | [Datadog](https://vagov.ddog-gov.com/dashboard/zsa-453-at7/ivc-champva-forms)          |
| Missing status update      | This is an upload with no corresponding status update from PEGA. | PEGA callbacks                | [Datadog](https://vagov.ddog-gov.com/dashboard/zsa-453-at7/ivc-champva-forms)          |
| Status update error        | PEGA attempted to update the status of an upload, but the call to the status update API received an error (non-200). | PEGA callbacks                | [Datadog](https://vagov.ddog-gov.com/dashboard/zsa-453-at7/ivc-champva-forms)          |
| Email confirmation attempt | VA notify was triggered in response to a submit.             | VA Notify - triggered         | VA Notify        |
| Email confirmation sent    | VA successfully sent the confirmation email. The VA Notify overall success rate is approx 85% and our success rate will likely be below 100%. | VA Notify - successfully sent | VA Notify        |
|                            |                                                              |                               |                  |
