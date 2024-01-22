---
title: "gRPC in Postman"
updated: 2024-01-19
contextual_links:
  - type: section
    name: "Additional resources"
  - type: subtitle
    name: "Videos"
  - type: link
    name: "Working with gRPC | The Exploratory"
    url: "https://youtu.be/RbHOs2xchGE"
  - type: link
    name: "Testing and Developing gRPC APIs | Postman Intergalactic"
    url: "https://youtu.be/QpHp1O3C5Zk?si=XZ3x8NYgOu4Kfy8v"
  - type: subtitle
    name: "Blog posts"
  - type: link
    name: "Postman v10 and gRPC: What You Can Do"
    url: "https://blog.postman.com/postman-v10-and-grpc-what-you-can-do/"
  - type: link
    name: "Understanding Asynchronous APIs"
    url: "https://blog.postman.com/understanding-asynchronous-apis/"
  - type: link
    name: "How to choose between REST vs. GraphQL vs. gRPC vs. SOAP"
    url: "https://blog.postman.com/how-to-choose-between-rest-vs-graphql-vs-grpc-vs-soap/"
  - type: subtitle
    name: "Public workspaces"
  - type: link
    name: "Public gRPC APIs"
    url:  "https://www.postman.com/devrel/workspace/public-grpc-apis"
---

Postman can make requests using _gRPC_, a schema-driven Remote Procedure Call (RPC) framework often used to enable inter-service communication. gRPC uses [protobuf (protocol buffer)](https://developers.google.com/protocol-buffers) files as its Interface Definition Language (IDL) to define API interfaces. This schema-driven approach simplifies inter-service communication, supports various languages, and boosts performance.

With gRPC requests in Postman, you can do the following, all without entering commands in the terminal or writing any code:

* View supported services and methods (with a service definition)
* Invoke a method
* Send a message payload
* View the response from the server
* Save example responses

As with other protocols in Postman, you can save gRPC requests in [collections](/docs/collections/collections-overview/) to reuse them later, share them with your teammates, or publish them to the community on [Postman's public API network](/docs/getting-started/first-steps/exploring-public-api-network/).

<img src="https://assets.postman.com/postman-docs/v10/grpc-echo-request-v10-3.jpg" alt="gRPC request interface">

## Next steps

To learn how to set up and invoke gRPC requests in Postman, see [Create a gRPC request](/docs/sending-requests/grpc/grpc-request-interface/) and [Invoke a gRPC request](/docs/sending-requests/grpc/first-grpc-request/).

You can learn about testing your gRPC requests in [Test and debug values in gRPC requests using JavaScript in Postman](/docs/sending-requests/grpc/scripting-in-grpc-request/) and [Write tests for gRPC requests using JavaScript assertions in Postman](/docs/sending-requests/grpc/test-examples/).

Simulating gRPC services is a valuable tool for testing and development. Learn more in [Create and use gRPC mock servers](/docs/sending-requests/grpc/using-grpc-mock/).

You can use the [Postman API Builder](/docs/designing-and-developing-your-api/the-api-workflow/) to create a service definition using protobuf IDL and keep it as a single source of truth for your API project. See [Manage service definitions for gRPC requests in Postman](/docs/sending-requests/grpc/using-service-definition/) to learn more.
