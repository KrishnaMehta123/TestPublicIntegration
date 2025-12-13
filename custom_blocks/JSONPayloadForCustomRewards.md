---
name: JSON Payload for Custom Rewards
---
# JSON Payloads

The following is an example payload for both types of custom rewards:

```json Physical & digital rewards
{
  "profiles": {
    "email": "jack@gmail.com",
    "identity": "foo",
    "phone": "+919538784114",
    "objectId": "g55b74fb10307"
  },
  "reward": {
    "clientRewardId": "110303",
    "clevertapRewardId": "20303",
    "rewardName": "PVR MOVIE TICKET",
    "rewardDescription": "Free PVR Movie ticket",
    "campaignId": 123494
  },
  "customMetadata": {
    "metadata key1": "value1",
    "metadata key2": "value2"
  }
}
```
```json Self-managed wallet credits
{
  "profiles": {
    "email": "jack@gmail.com",
    "identity": "foo",
    "phone": "+919538784114",
    "objectId": "g55b74fb10307"
  },
  "reward": {
    "clientRewardId": "110303",
    "clevertapRewardId": "20303",
    "rewardName": "PVR MOVIE TICKET",
    "rewardDescription": "Free PVR Movie ticket",
    "campaignId": 123494
  },
  "customMetadata": {
    "metadata key1": "value1",
    "metadata key2": "value2"
  }
}
```