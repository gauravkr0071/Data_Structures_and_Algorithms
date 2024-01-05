[Cache Coherence Problem and Approaches _ by Seralahthan _ Medium.pdf](https://github.com/gauravkr0071/Data_Structures_and_Algorithms/files/8011121/Cache.Coherence.Problem.and.Approaches._.by.Seralahthan._.Medium.pdf)

### __Cache Flush__
Flush does write back the contents of cache to main memory, and invalidate does mark cache lines as invalid so that future reads go to main memory.

## __Cache Coherence Problem and Approaches__

![image](https://user-images.githubusercontent.com/51910127/152683123-b743adef-8d3e-446b-99d6-7bfda6f0f891.png)

__What is a Cache Coherence Problem?__

Cache coherence is a concern raised in a multi-core system distributed L1 and L2 caches.
Each core has its own L1 and L2 caches and they need to always be in-sync with each
other to have the most up-to-date version of the data.

The Cache Coherence Problem is the challenge of keeping multiple local caches 
synchronized when one of the processors updates its local copy of data which is 
shared among multiple caches.

Imagine a scenario where multiple copies of same data exists in different caches
simultaneously, and if the processors are allowed to update their own copies freely,
an inconsistent view of memory can result.

For example, imagine a dual-core processor where each core brought a block of memory
into its private cache, and then one core writes a value to a specific location. When
the second core attempts to read that value from its cache, it will not have the most
recent version unless its cache entry is invalidated and a cache miss occurs. This 
cache miss forces the second core’s cache entry to be updated. To trigger the cache 
invalidation we need cache coherence policies. If there is no cache coherence policy
in-place, the wrong data would be read and invalid results would be produced, possibly
crashing the program.

__Cache Write Policies__

There two main cache write policies.

- __Write back__ : Write operations are usually made only to the cache. Main memory is only
 updated when the corresponding cache line is flushed from the cache.
 
- __Write through__ : All write operations are made to main memory as well as to 
the cache, ensuring that main memory is always valid.
From the above description it is clear that Write back policy results in 
inconsistency. If two caches contain the same line, and the line is updated in 
one cache, the other cache will unknowingly have an invalid value. Subsequently 
read to that invalid line produce invalid results.

But if we think deeper even the Write through policy also has consistency issues.
Even though memory is updated inconsistency can occur unless other cache monitor
the memory traffic or receive some direct notification of the update.

In order to solve these issue we introduce Cache Coherency Protocols.

Objective of any cache coherency protocol is to load the recently used
local variables into the appropriate caches and keep them through numerous
reads and writes, while using the protocol to maintain consistency of shared
variables that might be in multiple caches at the same time.

First let’s see what are the common ways of writing into a Cache before we jump
into the solutions to the Cache Coherence Problem.

__Write Through (WT) Protocol__

There are two fundamental implementations of the WT protocol.
- Write through with update protocol
- Write through with invalidation of copies

__Write through with update protocol__

When a processor writes a new value into its cache, the new value is also written
into the memory module that holds the cache block being changed. Some copies of this
block may exist in other caches, these copies must be updated to reflect the change
caused by the write operation.

We update the other cache copies by doing a broadcast with the updated data
to all processor modules in the system. Each processor module receives the broadcast
data, it updates the contents of the affected cache block if this block is present in
its cache.

__Write through with invalidation of copies__

When a processor writes a new value into its cache, this value is written
into the memory and all other copies in other caches are invalidated. This 
also done by broadcasting the invalidation request through the system. All 
caches receives this invalidation request and the cache which contains the 
updated data flushes its cache line.

__Write Back (WB) Protocol__

In the WB protocol, multiple copies of a cache block may exist if different processors
have loaded (read) the block into their caches.
In this approach if some processor wants to change this block,
it must first become the exclusive owner of the block.
When the ownership is granted to this processor by the memory module 
that is the home location of the block. All other copies, including 
the one in the memory module, are invalidated.

Now the owner of the block may change the contents of the memory.
When another processor wishes to read this block, the data are sent to this processor 
by the current owner. The data are also sent to the home memory module, which requires
ownership and updates the block to contain the latest value.

There are software level and hardware level solutions for cache coherence problem.

__CACHE MEMORY__
- [link](https://www.geeksforgeeks.org/cache-memory-in-computer-organization/)
