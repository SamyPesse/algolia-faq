There are two ways to delete your records: 

1.  For deleting a specific record, you need to know its `objectID` and pass it to the `index.deleteObject(objectID)` method.
2.  For deleting several records, you'll have to use the `index.deleteByQuery` method that will accept the exact same arguments as a normal search query, and will delete every record that match this query.