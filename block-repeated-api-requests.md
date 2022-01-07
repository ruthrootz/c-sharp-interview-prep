### incoming request data model
```
{
    requestRecord: 
    {
        JSON object, any form
    },
    clientId: string,
    transactionId: string,
    hash: string, added by our API
}
```

### record data model saved in DB
```
{
    record: {
        JSON object, any form
    },
    clientId: string,
    transactionId: string,
}
```

### pseudocode
- receive a POST/PUT request
- create a hash of the `requestRecord`
- check the cache for objects with a matching hash
    - if there's a matching `requestRecord`, stop processing request, return error
    - else, check cache for existing record with a matching `transactionId`
        - update and save record to cache
    - if there is no record with matching `transactionId` in the cache, check the DB
        - grab record from DB
        - update it
        - save it to cache
    - if there is no match in the DB, create a new record
        - save record to cache
- when a record outlives its cache time, save it to the DB before deleting it from the cache
- `requestRecord` objects can just be deleted from the cache when they run out of time

### NOTES
- cache stores the `record` objects we're trying to fill out and the `requestRecord` objects that we're using to fill in the data
- DB only stores records
- we're trying to block multiple IDENTICAL requests, even if they contain some of the same data for a given record
- record model is not known in advance
    - do we get `transactionId`?
    - do we know when a record is complete?
- records come from multiple different sources (`clientId`) in free-form JSON
- it might take multiple POST/PUT requests to fill out all the information needed for the record
  - i.e. the record might have to be updated multiple times
  - `transactionId` shows which record the `requestRecord` data belongs to
