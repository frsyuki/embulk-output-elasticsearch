# Elasticsearch output plugin for Embulk

## Overview

* **Plugin type**: output
* **Rollback supported**: no
* **Resume supported**: no
* **Cleanup supported**: no

## Configuration

- **nodes**: list of nodes. nodes are pairs of host and port (list, required)
- **index_name**: index name (string, required)
- **index_type**: index type (string, required)
- **doc_id_column**: document id column (string, default is null)
- **bulk_actions**: number of records buffered before sending the records to the cluster (int, default is 1000)
- **bulk_size_mb**: number of bytes in MB buffered before sending the records to cluster (double, default is 5.0)
- **concurrent_requests**: concurrent_requests (int, default is 5)

## Example

```yaml
out:
  type: elasticsearch
  node:
  - {host: localhost, port: 9300}
  index_name: <index name>
  index_type: <index type>
```

## Build

```
$ ./gradlew gem
```
