# MongoDB $inc operator error on non-numeric field
This bug demonstrates an error that occurs when using the `$inc` operator in MongoDB to update a field that is not a number. The `$inc` operator is designed to increment or decrement numeric values. If applied to a non-numeric field, it will result in an error.

## Bug Description
The `$inc` operator in MongoDB is used to increment a numeric field in a document. However, if this operator is applied to a field that does not have a numeric type (e.g., string, boolean), it will cause an error.

## Solution
Before using the `$inc` operator, ensure that the field you're targeting is of a numeric type. If not, use the `$set` operator to update the field with the new value.