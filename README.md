# Hash Table & Connections Network (CSE 331 Project)

This project implements an open-addressing hash table using **double hashing** and a simple **social-connection graph** built on top of it.

## Features

### 🔢 Hash Table
Implementation includes:
- `__setitem__`, `__getitem__`, `__delitem__`, `__contains__`
- Double hashing with `_hash_1` and `_hash_2`
- Automatic resizing via `_grow()`
- Support functions:
  - `update()`
  - `keys()`, `values()`, `items()`
  - `clear()`

Collision resolution uses:
- Primary hash → `_hash_1`
- Step size → `_hash_2`
- Probing until an empty or matching slot is found

Load factor > 0.5 triggers a table expansion.

### 👥 Connections (Graph BFS)
The `Connections` class uses a `HashTable` to store:
name -> list of friends

It supports:
- `add_connection(name, friend)`  
  Adds a friendship (ignores self-friendship).
- `check_if_related(p1, p2, n)`  
  Breadth-first search to determine if two people are connected within **n degrees of separation**.

### 📄 File
- `solution.py` — full implementation :contentReference[oaicite:0]{index=0}

## Summary
A complete custom hash table (double hashing + resizing) and a BFS-based relationship checker built on top of it.
