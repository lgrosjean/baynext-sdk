# Projects
(*projects*)

## Overview

### Available Operations

* [list](#list) - List all projects a user is a member of
* [create](#create) - Create a new project

## list

List projects for the current authenticated user.

### Example Usage

<!-- UsageSnippet language="python" operationID="list" method="get" path="/v1/projects" -->
```python
from baynext import Baynext
import os


with Baynext(
    server_url="https://api.example.com",
    http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
) as b_client:

    res = b_client.projects.list(limit=10, offset=0)

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `limit`                                                             | *OptionalNullable[int]*                                             | :heavy_minus_sign:                                                  | Number of projects to return                                        | 10                                                                  |
| `offset`                                                            | *OptionalNullable[int]*                                             | :heavy_minus_sign:                                                  | Number of projects to skip                                          | 0                                                                   |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |                                                                     |

### Response

**[List[models.ProjectPublic]](../../models/.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.BaynextDefaultError | 4XX, 5XX                   | \*/\*                      |

## create

Create a new project for the current authenticated user.

### Example Usage

<!-- UsageSnippet language="python" operationID="create_v1_projects_post" method="post" path="/v1/projects" -->
```python
from baynext import Baynext
import os


with Baynext(
    server_url="https://api.example.com",
    http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
) as b_client:

    res = b_client.projects.create(name="<value>")

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `name`                                                              | *str*                                                               | :heavy_check_mark:                                                  | N/A                                                                 |
| `description`                                                       | *OptionalNullable[str]*                                             | :heavy_minus_sign:                                                  | N/A                                                                 |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.ProjectCreated](../../models/projectcreated.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.BaynextDefaultError | 4XX, 5XX                   | \*/\*                      |