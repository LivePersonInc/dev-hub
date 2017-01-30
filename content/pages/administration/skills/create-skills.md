# Create skills

This API creates a list of skills for a specific account.

## Request

| Method  | URI | 
| :--------  | :----- |
| POST       | /api/account/{accountId}/configuration/le-users/skills |

**Request Headers**

| Header | Description |
| :----- | :---------- |
| Authorization | Contains token string to allow request authentication and authorization. |

**Request Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.

**Path Parameters**

| Parameter     | Description   | Type / Value  |
| :----------   | :------------ | :------------ |
| accountId     | LP site ID   | String ^[a-zA-Z0-9_]{1,20}$ |

## Response

**Response Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.

## Update skill

This API updates a skill for a specific account.

### Request

| Method | URI |
| :--------- | :-------- |
| PUT | /api/account/{accountId}/configuration/le-users/skills/{skillId} |

**Request Headers**

| Header | Description |
| :-------  | :------------  |
| Authorization | Contains token string to allow request authentication and authorization. |
| If-Match | Contains data revision as known by the client. Allows optimization of the backend, networking, and client resources utilization. |

**Request Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.

**Path Parameters**

| Parameter     | Description    | Type / Value |
| :-----------  | :------------  | :-------------- |
| accountId     | LP site ID     | String ^[a-zA-Z0-9_]{1,20}$ |
| skillId       | Skill ID       | Positive long number greater than zero |

### Response

**Response Body**

See [Appendix](appendix.md) for Entity Structure and Entity Example.
