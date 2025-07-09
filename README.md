# MIT6.824_DistributedSystems

This repository contains my implementations and notes for **MIT 6.824: Distributed Systems**, Spring 2025.  
Course site: [https://pdos.csail.mit.edu/6.824/](https://pdos.csail.mit.edu/6.824/)

# Table of Contents

- [MIT6.824_DistributedSystems](#mit6824_distributedsystems)
  - [Lecture 1: Introduction](#lecture-1-introduction)
  - [Lecture 2: Threads and RPC](#lecture-2-threads-and-rpc)
  - [Lecture 3: Raft – Consensus Algorithm](#lecture-3-raft--consensus-algorithm)
  - [Lecture 4: Raft Details + Lab Guide](#lecture-4-raft-details--lab-guide)
  - [Lecture 5: Fault Tolerance](#lecture-5-fault-tolerance)
  - [Lecture 6: Sharded Key/Value Storage](#lecture-6-sharded-keyvalue-storage)
  - [Lecture 7: Google File System (GFS)](#lecture-7-google-file-system-gfs)
  - [Lecture 8: HDFS + Storage Scalability](#lecture-8-hdfs--storage-scalability)
  - [Lecture 9: MapReduce](#lecture-9-mapreduce)
  - [Lecture 10: Distributed Transactions](#lecture-10-distributed-transactions)
  - [Lecture 11: Consistency Models](#lecture-11-consistency-models)
  - [Lecture 12: Spanner & Clock-Sync Systems](#lecture-12-spanner--clock-sync-systems)

## Lecture 1: Introduction

### What I mean by "distributed system":
A group of computers cooperating to provide a service.

### So why do people build distributed systems?
- to increase capacity via parallel processing
- to tolerate faults via replication
- to match distribution of physical devices e.g. sensors
- to increase security via isolation

## Lecture 2: Threads and RPC

- Concepts: concurrency, race conditions, Go RPC primitives.
- Goal: Build a basic RPC system using Go's interfaces and goroutines.
- Foundation for future labs.

## Lecture 3: Raft – Consensus Algorithm

- Problem: How can multiple nodes agree on a shared log?
- Raft simplifies consensus using leader election and log replication.
- Easier to understand than Paxos, Raft ensures safety and liveness.

## Lecture 4: Raft Details + Lab Guide

- Crash recovery, persistence, and log replay.
- How Raft handles term changes, commit index, and client redirection.
- Lab 2 expands from leader election to full consensus system.

## Lecture 5: Fault Tolerance

- How to build services that survive server/network crashes.
- Concepts: fail-stop, re-execution, heartbeats.
- Techniques: replication, deterministic execution, idempotency.

## Lecture 6: Sharded Key/Value Storage

- Scaling KV stores by partitioning across replicas.
- Rebalancing shards with configuration changes.
- Paxos or Raft used to agree on shard movements.

## Lecture 7: Google File System (GFS)

- GFS stores massive files across commodity servers.
- Design principles: chunk replication, master server, append-only writes.
- Focus on fault-tolerant storage and high throughput.

## Lecture 8: HDFS + Storage Scalability

- Hadoop Distributed File System inspired by GFS.
- Emphasis on batch read/write, replication, block placement.
- Tradeoffs in design: write-once-read-many, no random access.

## Lecture 9: MapReduce

- Review of MapReduce paper (Dean & Ghemawat)
- Hide parallelism and failure from the developer.
- Job scheduling, shuffle phase, deterministic execution.
## Lecture 10: Distributed Transactions

- Atomic commit using **Two-Phase Commit** (2PC)
- Failures during commit phases
- Paxos-based commit alternatives

## Lecture 11: Consistency Models

- Strong vs eventual consistency
- Linearizability, serializability, causal consistency
- Systems trade consistency for availability and performance

## Lecture 12: Spanner & Clock-Sync Systems

- Google's **Spanner**: a globally-consistent SQL database
- TrueTime API for clock uncertainty windows
- How Spanner achieves external consistency