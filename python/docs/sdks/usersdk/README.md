# UserSDK
(*user*)

## Overview

### Available Operations

* [get](#get) - Get Current User Details

## get

Get the current user.

This endpoint is used to retrieve the user information of the currently
authenticated user.

### Example Usage

<!-- UsageSnippet language="python" operationID="get_current_user_details_v1_user_me_get" method="get" path="/v1/user/me" -->
```python
from baynext import Baynext
import os


with Baynext(
    server_url="https://api.example.com",
    http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
) as b_client:

    res = b_client.user.get()

    # Handle response
    print(res)

```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `retries`                                                           | [Optional[utils.RetryConfig]](../../models/utils/retryconfig.md)    | :heavy_minus_sign:                                                  | Configuration to override the default retry behavior of the client. |

### Response

**[models.User](../../models/user.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.BaynextDefaultError | 4XX, 5XX                   | \*/\*                      |