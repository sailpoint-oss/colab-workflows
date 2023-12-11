Scheduled Full Source Aggregation for source that supports Delta Aggregation

This workflows runs a scheduled full source aggregation for a source enabled for delta aggregation. It uses HTTP Request to disable delta aggregation, then run a full aggregation for the source and finally reinstate the delta aggregation flag to true.

Please modify:
1. Modify the scheduled trigger time based on your needs.
2. The tenant name, client ID, secret and source ID in HTTP Request actions.
3. Add a Send Email action if an Admin notification is required.

Note: This HTTP Request URL will have to be modified once we receive a V3 or a BETA API replacement for loadAccounts CC API.