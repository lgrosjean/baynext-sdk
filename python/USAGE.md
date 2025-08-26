<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
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

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from baynext import Baynext
import os

async def main():

    async with Baynext(
        server_url="https://api.example.com",
        http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
    ) as b_client:

        res = await b_client.projects.list_async(limit=10, offset=0)

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->