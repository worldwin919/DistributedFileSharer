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
- Uses
