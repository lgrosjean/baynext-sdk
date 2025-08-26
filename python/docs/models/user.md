# User

User model.


## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `created_at`                                                         | [date](https://docs.python.org/3/library/datetime.html#date-objects) | :heavy_minus_sign:                                                   | N/A                                                                  |
| `updated_at`                                                         | [date](https://docs.python.org/3/library/datetime.html#date-objects) | :heavy_minus_sign:                                                   | N/A                                                                  |
| `id`                                                                 | *Optional[str]*                                                      | :heavy_minus_sign:                                                   | N/A                                                                  |
| `email`                                                              | *str*                                                                | :heavy_check_mark:                                                   | N/A                                                                  |
| `user_metadata`                                                      | [OptionalNullable[models.UserMetadata]](../models/usermetadata.md)   | :heavy_minus_sign:                                                   | N/A                                                                  |