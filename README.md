# Database Data Structures - Deep Dive

A comprehensive guide to **LSM Trees** and **B+ Trees**, the fundamental data structures powering modern databases.

## 🌐 Live Demo

Visit the interactive presentation: **[https://yourusername.github.io/data-structures-presentation](https://yourusername.github.io/data-structures-presentation)**

## 📚 What's Included

### 🌲 LSM Tree (Log-Structured Merge Tree)
Complete deep dive covering:
- **Architecture** - Memory and disk components (MemTable, SSTable, levels)
- **Write Operations** - WAL, fsync, memory flush process
- **Read Operations** - Multi-level search with Bloom filter optimization
- **Delete Operations** - Tombstone mechanism
- **Compaction** - Size-tiered, leveled, and time-window strategies
- **Level Structure** - L0 overlap problem and L1+ non-overlapping solution
- **MemTable** - Skip List implementation details
- **SSTable** - Complete file format with blocks, index, and metadata
- **Bloom Filters** - Algorithm, false positive rates, and performance impact

**Use Cases:** Write-heavy workloads, logging systems, time-series databases, metrics collection

**Used By:** Cassandra, RocksDB, LevelDB, HBase, ScyllaDB, InfluxDB

### 📊 B+ Tree (Balanced Plus Tree)
Concise overview covering:
- **Structure** - Balanced tree with high fanout
- **Operations** - Search, insert, delete, range queries
- **Disk Storage** - Node = page optimization, tree height calculations
- **Advantages** - Fast reads, excellent range scans
- **Disadvantages** - Slow random writes on HDD
- **Optimizations** - Buffer pool, WAL, group commit

**Use Cases:** Read-heavy workloads, OLTP databases, transactional systems

**Used By:** MySQL, PostgreSQL, SQLite, SQL Server, Oracle

## 🎯 Key Comparisons

| Aspect | LSM Tree | B+ Tree |
|--------|----------|---------|
| **Write Pattern** | Sequential (fast) | Random (slower) |
| **Write Throughput (HDD)** | 50,000-500,000/sec | 100-10,000/sec |
| **Read Performance** | Slower (multi-level) | Faster (single path) |
| **Range Scans** | Good | Excellent |
| **Space Efficiency** | 1.2-3x | 1.1-1.5x |
| **Background Work** | Heavy (compaction) | None |
| **Best For** | Write-heavy | Read-heavy |

## 🚀 Features

- ✅ **No Code** - Pure concepts and definitions
- ✅ **Visual Diagrams** - ASCII art showing structure
- ✅ **OS Details** - Sequential vs random I/O, seek time, fsync, page cache
- ✅ **Comparison Tables** - Side-by-side analysis
- ✅ **Responsive Design** - Works on all devices
- ✅ **Print-Friendly** - Perfect for presentations

## 🛠️ Local Development

```bash
# Clone the repository
git clone https://github.com/yourusername/data-structures-presentation.git

# Open in browser
cd data-structures-presentation
open index.html
```

## 📖 Topics Covered

### OS-Level Concepts
- Sequential vs Random I/O
- Seek time and rotational latency (HDD)
- fsync() and durability guarantees
- Page cache and buffer management
- Write amplification
- Read amplification

### Data Structure Concepts
- Write-Ahead Logging (WAL)
- Skip Lists
- Bloom Filters (probabilistic data structures)
- Prefix compression
- Compaction strategies
- Tree balancing

## 🎓 Perfect For

- Database engineers
- System designers
- Computer science students
- Technical presentations
- Interview preparation
- Architecture discussions

## 📝 License

MIT License - Feel free to use for educational purposes

## 🤝 Contributing

Contributions welcome! Feel free to:
- Open issues for corrections or improvements
- Submit PRs for additional content
- Suggest new topics

## 📧 Contact

Questions or feedback? Open an issue on GitHub!

---

**Note:** This is an educational resource. For production database implementations, always refer to official documentation and conduct thorough testing.
