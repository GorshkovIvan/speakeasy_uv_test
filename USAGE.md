<!-- Start SDK Example Usage [usage] -->
```python
# Synchronous Example
import os
from petstore import Petstore


with Petstore(
    api_key=os.getenv("PETSTORE_API_KEY", ""),
) as p_client:

    res = p_client.pet.update_pet(name="doggie", photo_urls=[
        "<value 1>",
    ], id=10, category={
        "id": 1,
        "name": "Dogs",
    })

    # Handle response
    print(res)
```

</br>

The same SDK client can also be used to make asynchronous requests by importing asyncio.
```python
# Asynchronous Example
import asyncio
import os
from petstore import Petstore

async def main():

    async with Petstore(
        api_key=os.getenv("PETSTORE_API_KEY", ""),
    ) as p_client:

        res = await p_client.pet.update_pet_async(name="doggie", photo_urls=[
            "<value 1>",
        ], id=10, category={
            "id": 1,
            "name": "Dogs",
        })

        # Handle response
        print(res)

asyncio.run(main())
```
<!-- End SDK Example Usage [usage] -->