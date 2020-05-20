# Root cause analysis for AES EDI problem 

## Date
2020-05-20

## Author
Aaron Sen Soner

## Status
Resolved

## Summary
Missing records not sent from AES EDI due to an issue with AES CIS service.

## Impact
486,000 records were affected.

## Root Cause
AES CIS service had an issue, which was logged under JIRA Issue AESCIS-38263.

## Trigger
Customer data was not sent from AES EDI.

## Resolution
Resend the file.

## Detection
JIRA Issue AESEDI-53447 was created.


## Action Items
| Action Item | Type | Owner | Bug |
| ----------- | ---- | ----- | --- |
| Improve verification of sent data from AES EDI. | prevent | Aaron Sen Soner | n/a **TODO** |
| Improve monitoring of AES CIS issues. | prevent | Aaron Sen Soner | n/a **TODO** |

## Lessons Learned
1. Identified the discrepancy with the EDI to CIS monitoring service.
2. Add additional layer of data verification once the customer data is sent.

## Timeline

2020-05-20 (*all times UTC*)

| Time  | Description |
| ----- | ----------- |
| 11:56 | Jira issue AESEDI-53447 was logged, customer data was discovered missing (486,000 records affected) |
| 13:00 | File was resent and customer data was processed |