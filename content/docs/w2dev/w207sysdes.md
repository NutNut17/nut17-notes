---
title: "System Design"
description: ""
summary: ""
date: 2025-07-09T23:44:01+08:00
lastmod: 2025-07-09T23:44:01+08:00
weight: 207
draft: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### Design Pattern

#### Creational Patterns

Factory
: An interface allows subclasses to alter the type of objects that will be created.

Builder
: Use a single constructor to construct complex objects step by step.

Singleton
: Ensure a class has only one instance and provide a global point of access to it.

#### Behavioral Patterns

Strategy
: Define a family of algorithms, encapsulate each one, and make them interchangeable.

Observer / PubSub
: Publisher updates to subscribers. Subscriber can subscribe to multiple publishers.

Iterator
: Provide a way to access elements of an aggregate object sequentially without exposing its underlying representation.

#### Structural Patterns

Adapter
: Convert the interface of a class into another interface clients expect.

Facade
: Abstract lower-level details.

### Concepts
