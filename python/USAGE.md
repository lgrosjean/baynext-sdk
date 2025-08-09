<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
from baynext_py import Baynext
import os


with Baynext(
    http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
) as baynext:

    res = baynext.projects.list(limit=10, offset=0)

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
from baynext_py import Baynext
import os

async def main():

    async with Baynext(
        http_bearer=os.getenv("BAYNEXT_HTTP_BEARER", ""),
    ) as baynext:

        res = await baynext.projects.list_async(limit=10, offset=0)

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->