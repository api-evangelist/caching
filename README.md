# Caching (caching)
An index and topic collection covering API-accessible caching services, in-memory data stores, key-value caches, and edge/CDN cache APIs. Caching reduces latency, lowers backend load, and improves API consumer experience by serving frequently requested data from memory or geographically distributed edges. This collection covers managed in-memory data stores like Redis, Amazon ElastiCache, and Google Cloud Memorystore; high-throughput alternatives such as Dragonfly, Aerospike, and Hazelcast; and edge cache services from Cloudflare, Fastly, Akamai, AWS CloudFront, and Vercel. It focuses on caching as a service or product, not on HTTP cache header semantics handled at the gateway or proxy layer.

**URL:** [https://apievangelist.com](https://apievangelist.com)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Cache, Caching, In-Memory Database, Edge Cache, Key-Value Store, CDN, Content Delivery Network

## Timestamps

- **Created:** 2026-05-19
- **Modified:** 2026-05-19

## Common Properties

- [Portal](https://apievangelist.com)
- [GitHubOrganization](https://github.com/api-evangelist)
- [JSONSchema - Cache Entry Schema](https://raw.githubusercontent.com/api-evangelist/caching/refs/heads/main/json-schema/caching-cache-entry-schema.json)
- [JSONSchema - Purge Request Schema](https://raw.githubusercontent.com/api-evangelist/caching/refs/heads/main/json-schema/caching-purge-request-schema.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/caching/refs/heads/main/json-ld/caching-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/caching/refs/heads/main/vocabulary/caching-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| In-Memory Key-Value Storage | Caching services like Redis, Memcached, and Valkey store data in RAM keyed by strings, hashes, or structured types, returning values in sub-millisecond response times for hot data paths. |
| Managed Cache as a Service | Cloud providers like Amazon ElastiCache, Google Cloud Memorystore, Azure Cache for Redis, and Upstash offer fully managed Redis and Memcached clusters with provisioning, patching, failover, and scaling handled by the provider. |
| Edge and CDN Caching | Services like Cloudflare, Fastly, Akamai, and AWS CloudFront cache API responses, static assets, and dynamic content at globally distributed edge locations to minimize latency for geographically dispersed consumers. |
| Cache Invalidation and Purge APIs | Edge and in-memory cache services expose purge, invalidate, and refresh endpoints that let applications evict stale entries by key, tag, surrogate-key, or URL pattern when underlying data changes. |
| TTL and Eviction Policies | Cache entries are governed by time-to-live values and eviction strategies (LRU, LFU, allkeys-lru, volatile-ttl) configurable per key or per cache instance to balance hit rates against memory pressure. |
| Distributed and Clustered Caches | Platforms like Hazelcast, Apache Ignite, GridGain, and Aerospike distribute cache data across multiple nodes with partitioning, replication, and near-cache support for large-scale, low-latency workloads. |
| Edge Key-Value Stores | Newer products like Cloudflare Workers KV, Vercel Edge Config, Akamai EdgeKV, and Fastly KV Store expose programmatic key-value APIs at the edge, blending CDN distribution with application state. |
| Cache Tagging and Surrogate Keys | Edge caches like Fastly and Cloudflare support surrogate keys and cache tags that group related objects so a single purge request can invalidate thousands of related entries atomically. |

## Use Cases

| Name | Description |
|------|-------------|
| Session and Token Caching | Cache authenticated sessions, JWTs, and OAuth tokens in Redis or Memcached so API gateways can validate requests without round-tripping to an identity provider on every call. |
| API Response Caching | API gateways and edge networks cache GET responses keyed by URL and headers so repeated requests for the same resource are served from cache. |
| Database Query Result Caching | Backend services cache expensive database query results in Redis or Hazelcast with TTLs so subsequent identical queries return immediately. |
| Rate Limiting and Counters | Redis and similar in-memory stores back distributed rate limiters, leaderboards, and counters using atomic increment operations. |
| CDN Static Asset Delivery | Cloudflare, Fastly, CloudFront, and Akamai cache images, JavaScript, CSS, and other static assets at edge POPs to serve global users with low latency. |
| Edge Personalization and Feature Flags | Edge KV stores like Vercel Edge Config and Cloudflare Workers KV hold feature flags, A/B test configurations, and personalization data accessed by edge functions. |
| Real-Time Leaderboards and Pub/Sub | Redis sorted sets and pub/sub channels power real-time leaderboards, chat backends, and notification fanout patterns. |
| Pre-Warming and Cache Stampede Prevention | Applications pre-populate caches before traffic spikes and use Redis-backed singleflight to prevent thundering herds against origin systems. |

## Integrations

| Name | Description |
|------|-------------|
| Redis | The most widely deployed open source in-memory data structure store, supporting strings, hashes, sets, sorted sets, streams, and pub/sub with sub-millisecond latency. |
| Amazon ElastiCache | Fully managed in-memory cache service from AWS supporting Redis and Memcached engines with multi-AZ failover and seamless EC2 integration. |
| Google Cloud Memorystore | Google Cloud's managed Redis and Memcached service with VPC integration, automatic patching, and high-availability replication. |
| Azure Cache for Redis | Microsoft's managed Redis service offering Basic, Standard, Premium, and Enterprise tiers with geo-replication and persistence. |
| Upstash | Serverless Redis and Kafka platform with per-request pricing, global replication, and an HTTP-based REST API for edge and serverless workloads. |
| Cloudflare | Global edge network providing CDN caching, Workers KV, R2, Cache API, and surrogate-key purging across 300+ POPs worldwide. |
| Fastly | Real-time edge cloud platform with instant purge, surrogate keys, VCL-based cache configuration, and the Fastly KV Store for edge state. |
| Akamai Technologies | Enterprise CDN and edge platform with EdgeKV key-value storage, Ion delivery, and global edge caching across the world's largest distributed network. |
| Vercel | Frontend cloud with Edge Config, KV (powered by Upstash), and CDN caching for Next.js and other frameworks deployed to its global edge network. |
| Hazelcast | Open-source in-memory data grid for distributed caching, stream processing, and real-time analytics across clustered Java and polyglot applications. |

## Artifacts

Machine-readable API specifications organized by format.

### JSON Schema

- [Cache Entry Schema](json-schema/caching-cache-entry-schema.json)
- [Purge Request Schema](json-schema/caching-purge-request-schema.json)

### JSON Structure

- [Cache Entry Structure](json-structure/caching-cache-entry-structure.json)
- [Purge Request Structure](json-structure/caching-purge-request-structure.json)

### JSON-LD

- [Caching Context](json-ld/caching-context.jsonld)

## Vocabulary

- [Caching Vocabulary](vocabulary/caching-vocabulary.yaml) — Unified taxonomy mapping resources, actions, workflows, and personas across in-memory caches, key-value stores, and edge CDN caching services

## Network

This index references the following caching, in-memory data store, and edge cache repositories:

- [Aerospike](https://github.com/api-evangelist/aerospike)
- [Akamai Technologies](https://github.com/api-evangelist/akamai-technologies)
- [Amazon CloudFront](https://github.com/api-evangelist/amazon-cloudfront)
- [Amazon ElastiCache](https://github.com/api-evangelist/amazon-elasticache)
- [Amazon MemoryDB](https://github.com/api-evangelist/amazon-memorydb)
- [Apache Geode](https://github.com/api-evangelist/apache-geode)
- [Apache Ignite](https://github.com/api-evangelist/apache-ignite)
- [Azure Cache for Redis](https://github.com/api-evangelist/microsoft-azure-cache-for-redis)
- [Azure Front Door](https://github.com/api-evangelist/microsoft-azure-front-door)
- [CloudFront](https://github.com/api-evangelist/cloudfront)
- [Cloudflare](https://github.com/api-evangelist/cloudflare)
- [Cloudflare.com](https://github.com/api-evangelist/cloudflare-com)
- [Couchbase](https://github.com/api-evangelist/couchbase)
- [Dragonfly](https://github.com/api-evangelist/dragonfly)
- [Etcd](https://github.com/api-evangelist/etcd)
- [Fastly](https://github.com/api-evangelist/fastly)
- [Google Cloud CDN](https://github.com/api-evangelist/google-cloud-cdn)
- [Google Cloud Memorystore](https://github.com/api-evangelist/google-cloud-memorystore)
- [GridGain](https://github.com/api-evangelist/gridgain)
- [HashiCorp Consul](https://github.com/api-evangelist/consul)
- [Hazelcast](https://github.com/api-evangelist/hazelcast)
- [Imgix](https://github.com/api-evangelist/imgix)
- [KVdb](https://github.com/api-evangelist/kvdb)
- [NATS](https://github.com/api-evangelist/nats)
- [Netlify](https://github.com/api-evangelist/netlify)
- [QuantCDN](https://github.com/api-evangelist/quantcdn)
- [Redis](https://github.com/api-evangelist/redis)
- [Redis Streams](https://github.com/api-evangelist/redis-streams)
- [Riak KV](https://github.com/api-evangelist/riak)
- [Squid](https://github.com/api-evangelist/squid)
- [Upstash](https://github.com/api-evangelist/upstash)
- [Varnish Cache](https://github.com/api-evangelist/varnish)
- [Vercel](https://github.com/api-evangelist/vercel)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
