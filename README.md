# Hive 3 and Spark Integration

## Summary

The Hive Metastore has evolved from Hive 1/2 and now includes the concept of a "Catalog".  Historically, Hive and Spark shared the same 'metadata' space.  So tables (at least the table definitions) created by either could be seen by the other.

But as the two technologies have diverged, the incompatibilities has grown.  And in Hive 1.1 those incompatibilities often lead to 'silent' data issues.

I'll cover how workloads / pipelines need to adjusted to address the architectural changes imposed by the Hive Metastore to eliminate data issues between these two SQL engines.

## Pipeline Behaviors

