### RUN QUERY

```SELECT sequence_schema, sequence_name 
FROM information_schema.sequences 
ORDER BY sequence_name ```

### THEN

chaneg the_primary_key_sequence which show on the before query and change the_table with table errors duplicate
```
SELECT setval('the_primary_key_sequence', (SELECT MAX(the_primary_key) FROM the_table)+1);
```


