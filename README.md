# ParcelPulse — AI-Assisted Delivery Intelligence & Recovery Platform

An event-driven shipment intelligence platform built with **Java, Spring Boot, Apache Kafka, Redis, PostgreSQL, and React**, designed to track deliveries, detect shipment disruptions, and coordinate recovery workflows. Integrates an **LLM-powered assistant with Retrieval-Augmented Generation (RAG)** to provide contextual shipment explanations and delivery support.

## Overview

Traditional shipment tracking systems primarily display delivery status updates, leaving customers and logistics operators with limited visibility into delays, failed deliveries, and shipment exceptions.

ParcelPulse takes a proactive approach by processing shipment events in real time, identifying delivery disruptions, and coordinating recovery workflows through an event-driven architecture.

The platform uses Apache Kafka to decouple shipment services and support asynchronous event processing. It incorporates idempotent event handling, shipment lifecycle management, and automated exception workflows to improve reliability across distributed components.

An AI-powered shipment assistant uses retrieval-augmented generation (RAG) to answer customer queries using shipment history and delivery policies, providing contextual explanations grounded in platform data.

## Key Features

- Real-time shipment tracking and delivery status updates
- Event-driven shipment processing using Apache Kafka
- Detection of delayed, duplicate, and failed delivery events
- Shipment lifecycle management using state-based workflows
- Idempotent event processing to prevent duplicate updates
- Automated exception handling and delivery recovery workflows
- Redis-based caching for frequently accessed shipment data
- PostgreSQL-backed shipment and event persistence
- AI-powered shipment assistant using LLMs and RAG
- Contextual retrieval from shipment history and delivery policies
- RESTful APIs for shipment and tracking operations
- Dockerized multi-service deployment

## System Architecture

### Components

**Shipment Service**
- Creates and manages shipment records
- Maintains shipment lifecycle and delivery status
- Exposes REST APIs for shipment operations

**Event Processing Service**
- Consumes shipment events through Apache Kafka
- Processes tracking updates asynchronously
- Detects duplicate, delayed, and invalid events
- Updates shipment state while maintaining event consistency

**Recovery & Exception Service**
- Identifies failed deliveries and shipment exceptions
- Coordinates recovery workflows based on shipment state
- Handles retries and failed event processing
- Supports escalation of unresolved delivery issues

**AI Assistant Service**
- Uses an LLM-powered conversational interface
- Retrieves relevant shipment history and delivery policies through RAG
- Provides contextual explanations for delivery delays and exceptions
- Uses controlled backend API calls for current shipment information

**Kafka Event Bus**
- Publishes shipment lifecycle events
- Decouples services through asynchronous messaging
- Supports shipment updates and recovery workflows

**PostgreSQL**
- Stores shipment records, tracking history, and operational data
- Maintains persistent shipment state

**Redis Cache**
- Caches frequently accessed shipment information
- Reduces repeated database lookups
- Improves tracking API response performance

## Event Flow

1. A shipment is created through the Shipment Service.
2. Shipment lifecycle events are published to Kafka.
3. The Event Processing Service consumes and validates incoming events.
4. Shipment status and tracking history are updated in PostgreSQL.
5. Delayed or failed shipments are identified through exception detection rules.
6. The Recovery Service initiates the appropriate recovery workflow.
7. Customers can query shipment information through the AI assistant, which retrieves relevant context and uses backend APIs when live data is required.

## Technology Stack

**Backend**
- Java 21
- Spring Boot
- Spring Data JPA
- Spring Web

**Messaging & Event Processing**
- Apache Kafka

**Database & Caching**
- PostgreSQL
- Redis

**AI Integration**
- Large Language Models (LLMs)
- Retrieval-Augmented Generation (RAG)
- Embeddings and semantic retrieval

**Frontend**
- React
- TypeScript

**DevOps**
- Docker
- Docker Compose

## Engineering Focus

ParcelPulse explores core distributed systems and backend engineering concepts:

- Event-driven architecture and asynchronous communication
- Idempotency and duplicate event handling
- State management and workflow orchestration
- Database consistency and transaction management
- Retry strategies and fault recovery
- Caching and API performance optimization
- LLM integration with retrieval-grounded responses

## Project Goals

Build a reliable shipment intelligence platform that goes beyond conventional tracking by combining distributed backend processing, automated delivery exception handling, and practical AI-powered customer assistance.
