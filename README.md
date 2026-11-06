A scalable distributed file-sharing platform built with Java, Spring Boot, Apache Kafka, Redis, PostgreSQL, and Docker. The system enables peer discovery, file metadata management, asynchronous file synchronization, and fault-tolerant communication between distributed nodes.

# Overview

Traditional centralized file-sharing systems suffer from single points of failure and scalability limitations. This project explores distributed system principles by enabling multiple nodes to share, discover, and synchronize files while maintaining consistency and reliability.

The platform leverages an event-driven architecture using Apache Kafka to decouple services and support asynchronous processing for file indexing, replication, and peer notifications.

# Key Features
Peer-to-peer file sharing across distributed nodes
File upload and download APIs
Metadata management and indexing
Event-driven communication using Apache Kafka
Distributed file synchronization
Redis-powered metadata caching
Fault-tolerant message processing
Dockerized multi-service deployment
RESTful APIs for client interactions
Structured logging and error handling

# System Architecture
Components
Metadata Service
Maintains file metadata
Tracks file ownership and availability
Stores metadata in PostgreSQL
Peer Nodes
Store actual file content
Handle uploads and downloads
Communicate through platform APIs
Kafka Event Bus
Publishes file events
Enables asynchronous communication
Handles indexing, synchronization, and replication workflows
Redis Cache
Caches frequently accessed metadata
Improves lookup performance
Reduces database load

# Technology Stack
Backend
Java 21
Spring Boot
Spring Data JPA
Spring Web
Messaging & Streaming
Apache Kafka
Storage
PostgreSQL
Caching
Redis
DevOps
Docker
Docker Compose
Event Flow
ching
