
# topics:

## PLPGSQL
rls
triggers
functions

postgrest
## toast and file storage with bytea

  
[TOAST](https://www.postgresql.org/docs/current/static/storage-toast.html) is a mechanism PostgreSQL uses to keep physical data rows from exceeding the size of a data block (typically 8KB). Postgres does not support physical rows that cross block boundaries, so the block size is a hard upper limit on row size. To allow user tables to have rows wider than this, the TOAST mechanism breaks up wide field values into smaller pieces, which are stored "out of line" in a TOAST table associated with the user table.

Each table you create has its own associated (unique) TOAST table, which may or may not ever end up being used, depending on the size of rows you insert. All of this is transparent to the user, and enabled by default.

When a row that is to be stored is "too wide" (the threshold for that is 2KB by default), the TOAST mechanism first attempts to compress any wide field values. If that isn't enough to get the row under 2KB, it breaks up the wide field values into chunks that get stored in the associated TOAST table. Each original field value is replaced by a small pointer that shows where to find this "out of line" data in the TOAST table. TOAST will attempt to squeeze the user-table row down to 2KB in this way, but as long as it can get below 8KB, that's good enough and the row can be stored successfully.

All standard Postgres data types that could possibly have values wider than 2KB support being "TOASTed" in this way, and so do most potentially-wide extension data types.

You can view the current TOAST options for a table by opening psql and running

### When is it bad idea to store binary files in the database?

Very large files (100MB+), where performance is critical to the application. The database layer adds a lot of overhead and complexity that may not be required.

## ACID
In [database systems](https://en.wikipedia.org/wiki/Database_system "Database system"), **ACID** is an acronym for **[atomicity](https://en.wikipedia.org/wiki/Atomicity_\(database_systems\) "Atomicity (database systems)")**, **[consistency](https://en.wikipedia.org/wiki/Consistency_\(database_systems\) "Consistency (database systems)")**, **[isolation](https://en.wikipedia.org/wiki/Isolation_\(database_systems\) "Isolation (database systems)")**, and **[durability](https://en.wikipedia.org/wiki/Durability_\(database_systems\) "Durability (database systems)")**: four properties used to characterize reliable [database transactions](https://en.wikipedia.org/wiki/Database_transaction "Database transaction").[[1]](https://en.wikipedia.org/wiki/ACID#cite_note-HarderReuter1983-1) Together, the properties describe how a transaction behaves with respect to failure, database invariants, concurrent execution, and persistence after commit.