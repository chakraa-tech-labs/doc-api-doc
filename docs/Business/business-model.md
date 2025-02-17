---
sidebar_position: 1
---
# Object Model 


### Object Model
```json
{
  "id": "20923000000058880",
  "org_id": "10078971418", // Read-only
  "waba_id": "327792133761974", // Read-only
  "super_admin_id": "20923000000064161", // Read-only
  "name": "VK55 org", // Mandatory, writable
  "time_zone": "Asia/Dubai", // Editable
  "configs": {
    "mandate_log_conversation": true, // false
    "share_read_receipts": true, // false
    "chat_onboarding": {} // Explained in the Chat Onboarding section
  },
  "waba_info": {
    "account_status": "connected", // scheduled_for_disable, disabled, revoked, deleted
    "disable_time": "2024-10-10 12:00:00",
    "latest_violation": "SOME_REASON",
    "restriction_info": {
      "RESTRICTION_ADD_PHONE_NUMBER_ACTION": "2024-10-10 12:00:00",
      "RESTRICTED_BIZ_INITIATED_MESSAGING": "2024-10-10 12:00:00",
      "RESTRICTED_CUSTOMER_INITIATED_MESSAGING": "2024-10-10 12:00:00"
    },
    "verified": true,
    "review_status": "REJECTED",
    "max_daily_conversation_per_phone": 1000,
    "max_phone_numbers_per_business": 100,
    "max_phone_numbers_per_waba": 100,
    "increased_capabilities_status": "NEED_MORE_INFO" // DEFERRED, FAILED
  },
  "channels": [{}, {}]
}
```

