# AWS EC2

## General Purpose Instances

---

## 1. EC2 Instance Types

- EC2 instances are divided into **7 main types**
- **Instance Type ≠ Purchasing Option**
  - Instance Type → hardware configuration
  - Purchasing Option → pricing model (On-Demand, Reserved, Spot)

---

## 2. What are General Purpose Instances?

- Provide a **balanced combination** of:
  - Compute (CPU)
  - Memory (RAM)
  - Networking
- Resources are **average**
- Suitable for **general-purpose applications**

---

## 3. Use Cases

- Can be used for a **variety of workloads**
- Best when no special optimization is required
- Common use cases:
  - Web applications
  - Development and testing
  - Small to medium databases

---

## 4. General Purpose Instance Series

General Purpose instances have **three series**:

### A Series

- Example: `A1`
- Available sizes:
  - Medium
  - Large
- ❌ Nano, Micro, Small are **not available**

---

### M Series

- Examples:
  - `M4`
  - `M5`, `M5a`, `M5ad`, `M5d`
- `M3` is deprecated
- ⚠️ **M does NOT mean Memory Optimized**
- M Series belongs to **General Purpose**

---

### T Series

- Examples:
  - `T2`, `T3`, `T3a`
- Commonly used for labs and practice

---

## 5. Free Tier Instance

- **T2.micro**
  - Part of General Purpose instances
  - **Free Tier eligible**
- Not all instance types are free tier eligible

---

## 6. Instance Sizes

Common EC2 instance sizes:

| Size   | Description            |
| ------ | ---------------------- |
| Nano   | Smallest configuration |
| Small  | Low configuration      |
| Medium | Moderate configuration |
| Large  | High configuration     |

- Larger size = more vCPUs and RAM
- Not all sizes are available in every series

---

## 7. Important Note (Interview)

**Question:** Can we create a Nano instance in A Series?
**Answer:** ❌ No
Reason: A Series supports **only Medium and Large** sizes

---

### M Series

- Only **Large** size is available
- ❌ Medium, Small, Nano are **not available**
- Used when consistent performance is required

---

### T Series

- All sizes are available:
  - Nano
  - Micro
  - Small
  - Medium
  - Large
- **T2.micro** belongs to this series
- Micro size is considered part of the Nano/Small family

---

## A1 Instance Series

### Overview

- A1 instances are **ideally suited for scale-out workloads**
- Built for workloads supported by the **ARM ecosystem**

---

### What is ARM Ecosystem?

- ARM is a processor architecture
- Commonly used for:
  - Lightweight workloads
  - Scalable applications
  - Container-based environments
- Optimized for efficiency and cost

---

### Scale-Out Workloads

- Start with low configuration
- Easily scale when sudden high load occurs
- Useful when traffic or usage increases unexpectedly

---

## Best Use Cases for A1 Instances

### 1. Containerized Microservices (Most Important)

- Designed for:
  - Docker
  - Kubernetes
- Microservices:
  - Perform a **single specific task**
  - Lightweight
  - Fast startup
- Multiple microservices can run in containers

---

### 2. Web Servers

- Used to host websites
- Accessible via:
  - HTTP
  - HTTPS

---

## Containers vs Virtual Machines

### Virtual Machine Environment

- Infrastructure layer
- Host OS / Hypervisor (e.g., ESXi)
- Guest OS (Windows/Linux)
- Binaries and libraries installed
- Application runs on top
- Heavy and slower to start

---

### Containerized Environment

- Infrastructure layer
- Operating System
- Containers run **directly on OS**
- No separate Guest OS
- Multiple applications run inside containers
- Lightweight and fast
- Efficient resource usage

---

## Container Benefits

- Faster startup
- Lightweight
- High scalability
- Efficient resource utilization
- Widely used in cloud environments

---

### Popular Container Technologies

- Docker
- Kubernetes

## A1 Instances – Extended Use Cases

- Ideal for workloads using containerization
- Used for:
  - Containerized microservices
  - Web servers
  - Caching fleets
  - Distributed data stores
  - Applications requiring ARM instruction set
- Optimized for ARM-based workloads
- Suitable for scale-out workloads

---

## Key A1 Instance Points to Remember

- Built on ARM ecosystem
- Supports lightweight and scalable applications
- Best choice for:
  - Containers
  - Microservices
  - Distributed systems
- Important keywords to remember for exams:
  - Web servers
  - Containerization
  - Caching fleets
  - Distributed data stores
  - ARM instruction set

---

## M Series Instances (General Purpose)

- Available instance types:

  - M4
  - M5
  - M5a
  - M5ad
  - M5d
- Most commonly used:

  - M4
  - M5
- M5ad and M5d are recently added variants

---

## M4 Instances

- Uses Intel Xeon processor
- Optimized for EC2 workloads
- Uses Nitro hypervisor
- Designed for high-performance workloads
- Only **Large** size is available
- vCPU range:
  - 2 to 40 virtual CPUs
- Memory range:
  - 8 GB to 160 GB RAM
- Instance storage:
  - EBS-only
- Root volume must be EBS
- Additional storage can be attached separately

---

## M5 / M5a / M5ad / M5d Instances

- Provide an ideal cloud infrastructure
- Balanced compute, memory, and networking resources
- Suitable for a broad range of applications
- Higher performance than M4
- Better:
  - CPU performance
  - RAM management
  - Network bandwidth
  - Storage throughput
- Lower latency compared to M4

---

## M5 Instance Specifications

- vCPU range:
  - 2 to 96 virtual CPUs
- Memory range:
  - 8 GB to 384 GB RAM
- Supports larger and more demanding applications
- Preferred over M4 for large-scale workloads

---

## Storage in M5 Instances

- Uses EBS for root volume
- High throughput and low latency storage
- Suitable for enterprise-level applications

## M5 Storage and Performance Enhancements

- M5 supports higher RAM compared to M4
- Maximum RAM:
  - M4: 8 up to 160 GB
  - M5,M5a,M5ad,M5d: 8 up to 384 GB
- Storage options in M5:
  - EBS
  - NVMe SSD (Nitro-based)
- NVMe SSD is used in high-end instances
- NVMe is preferred when:
  - Higher RAM is required
  - High throughput is needed
  - Low latency is required
  - High network bandwidth is required (up to 25 Gbps)

---

## Key Storage Notes

- M4 supports only EBS
- M5 supports both EBS and NVMe SSD
- NVMe is used for better performance
- High-performance workloads prefer NVMe-backed instances

---

## T Series Instances (General Purpose)

- Includes:
  - T2
  - T3
  - T3a
- T2.micro is **Free Tier eligible**
- Designed for:
  - Development
  - Testing
  - Small workloads

---

## When to Use T Series

- Application development
- Testing new applications
- Website testing
- Proof-of-concept environments
- Early-stage projects

---

## When NOT to Use T Series

- Production workloads
- High-performance applications
- Real-time heavy workloads

---

## Performance Characteristics of T Series

- Provides baseline CPU performance
- CPU utilization range:
  - Minimum: ~5%
  - Maximum baseline: ~40%
- Not suitable for workloads requiring:
  - 80–100% CPU utilization

---

## Burstable Performance Concept

- T series supports burstable CPU performance
- CPU can temporarily exceed baseline when required
- Bursting allows short-term performance spikes
- Designed for intermittent workloads

---

## Unlimited Mode (T Series)

- Unlimited instances can sustain high CPU performance
- Suitable for occasional CPU-intensive bursts
- Instances are low-cost
- Can be created and used for long durations

---

## Resource Limitations of T Series

- Limited vCPU count
- Maximum vCPU capacity is low
- Not designed for heavy compute workloads
- Best suited for lightweight and temporary tasks

---

## Summary of T Series

- Low performance
- Very cost-effective
- Best for development and testing
- Free Tier support available
- Burstable CPU but limited overall capacity

## T Series – Resource Limits and Capabilities

- Limited vCPU capacity
- Maximum virtual CPUs are low
- Not suitable for high-performance production workloads
- Can be used to test sustained high CPU performance in controlled scenarios

---

## T Series – Memory and Network

- RAM range:
  - 0.5 GB to 32 GB
- Provides very basic memory configuration
- Network bandwidth is limited
- Maximum network bandwidth is approximately 5 Gbps
- Suitable only for lightweight workloads

---

## T Series – Common Use Cases

- Website hosting (small-scale)
- Web application development
- Code repositories
- Application development environments
- Build and test environments
- Testing containerized microservices
  - Docker
  - Kubernetes
- Suitable for small and non-critical applications

---

## Overall Summary of General Purpose Instances

- General Purpose instances provide balanced resources
- Designed for a wide range of workloads
- Three General Purpose instance series:
  - A Series
  - M Series
  - T Series

---

## Key Revision Questions

- What are the three General Purpose instance series?

  - A Series
  - M Series
  - T Series
- Which series provides the maximum RAM?

  - M Series
  - Specifically M5 instances
- How many total EC2 instance types exist?

  - Seven types

---


---
---

## Final Notes

- General Purpose instances should now be clear
- Practice recalling:

  - Instance series
  - Use cases
  - Performance characteristics
