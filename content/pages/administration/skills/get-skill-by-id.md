# Get skill by ID

This API retrieves a single skill (by ID) for a specific account.

## Request

| Method     | URI                |
| :--------  | :----------------- |
| GET        | /api/account/{accountId}/configuration/le-users/skills/{skillId}|

**Request Headers**

| Header         | Description                                |
| :------------  | :---------------------                     |
| Authorization  | Contains token string to allow request authentication and authorization. |

**Request Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.

**Path Parameters**

| Parameter      | Description     | Type / Value             |                               
| :------------  | :-------------  | :-----------------          |                              
| accountId      | LP site ID      | String ^[a-zA-Z0-9_]{1,20}$ |
| skillId        | Skill ID        | Positive long number greater than zero |

## Response

**Response Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.
