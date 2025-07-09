# 6.824_DistributedSystems

My implementations and notes for **MIT 6.824: Distributed Systems** (Prof. Robert Morris, MIT CSAIL).

📚 **Course materials & schedule**: https://pdos.csail.mit.edu/6.824/schedule.html

## 🧠 What’s Inside

- Go-based labs:
  - **Lab 1**: RPC library
  - **Lab 2**: Raft (leader election, log replication, persistence)
  - **Lab 3**: Key/value service (sharded version optional)
  - **Lab 4**: MapReduce framework *(optional)*
- `notes/` directory: summaries of key lectures, papers, and DDIA chapters

## 🚀 Getting Started

### Prerequisites

- Go 1.18+ installed  
- Unix-like OS (Linux/macOS/WSL)  
- Git  

### Setup & Running Tests

```bash
git clone https://github.com/zhangxijing97/MIT6.824_DistributedSystems.git
cd MIT6.824_DistributedSystems

# Example: run Raft tests
cd lab2_raft
go test -race ./...
