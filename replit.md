# HashMap Lab - C Educational Project

## Overview
This is an educational C project where students implement a HashMap (Hash Table) data structure using open addressing (linear probing) for collision resolution.

## Project Structure
- `hashmap.h` - Header file with struct definitions and function declarations
- `hashmap.c` - Student implementation file (functions to be filled in)
- `main.c` - Sample application: word frequency counter using the HashMap
- `test.c` - Unit tests for all HashMap functions
- `test.sh` - Shell script for compiling and running tests with git tracking

## Key Data Structures
- `Pair` - Stores a `char* key` and `void* value`
- `HashMap` - Contains `Pair** buckets`, `long size`, `long capacity`, `long current`

## Functions to Implement (in hashmap.c)
1. `createMap(capacity)` - Allocate and initialize the HashMap
2. `insertMap(map, key, value)` - Insert with linear probing collision resolution
3. `searchMap(map, key)` - Search by key, stop at NULL bucket
4. `eraseMap(map, key)` - Soft-delete by setting `pair->key = NULL`
5. `firstMap(map)` - Return first valid Pair
6. `nextMap(map)` - Return next valid Pair from current index
7. `enlarge(map)` - Double capacity and rehash all valid elements

## Build & Run
- **Build main app**: `gcc -g main.c hashmap.c -o main -lm && ./main`
- **Run tests**: `bash test.sh`

## Workflow
- "Run HashMap" workflow compiles and runs main.c

## Notes
- The `hashmap.c` file contains student exercises — do not modify the function stubs or comments
- Collision resolution uses linear probing with circular array indexing
- Soft deletion: invalidate pairs by setting `key = NULL` (not freeing the pair)
- The `enlarge_called` global flag is used by the test suite
