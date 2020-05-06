# Tutorial GraphQL Schema Introspection 101 

This tutorial was first published on May 5, 2020.

## Tutorial Overview

GraphQL is a query language based on a type system. GraphQL types define what objects are supported, what fields are associated with an object, and what can be queried and how, all defined by the GraphQL schema. To be able to use GraphQL APIs effectively, it is essential to have a good understanding of the InfoHub schema. 

Although the InfoHub GraphQL schema can be accessed through the [GitHub repo](https://github.ibm.com/SC-Shared-Services/infohub-graphql-server-base/blob/master/src/main/resources/schema.graphqls), there is another way to get information on the schema from the live system: using GraphQL Introspection. Schema introspection can be a very handy tool whenever you have a question about any part of the schema, such as what objects are defined, what fields are associated with a type, what are the values of an enumeration, what kind of queries are supported, and what parameters can be used for a query, etc.

## What you will learn

At the end of this tutorial, you will learn:

..* How to find all the supported types (objects, interfaces, enum, etc.)
..* How to find more details of each type (such as fields for an object, or values of an enum)
..* What queries are supported, and query details (such as parameters)
..* What mutations are supported
..* How to construct a GraphQL query based on introspection results

