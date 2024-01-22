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

## Developing gRPC APIs with Postman

If you haven't already, [download and install the Postman desktop app](/docs/getting-started/installation/installation-and-updates/) to get started.

Using a gRPC request, you can view supported services and methods (with a service definition), invoke the method of your interest, send a message payload, view the response from the server, and save example responses, all without entering commands in the terminal or writing any code. You can save these requests into a collection to reuse them later, share them with your teammates, or publish them to the community on [Postman's public API network](/docs/getting-started/first-steps/exploring-public-api-network/).

You can use the [Postman API Builder](/docs/designing-and-developing-your-api/the-api-workflow/) to create the service definition using protobuf IDL and keep it as a single source of truth for your API project.

<img src="https://assets.postman.com/postman-docs/v10/grpc-echo-request-v10-3.jpg" alt="gRPC request interface">

## Next steps

To learn how to set up and invoke gRPC calls in Postman, see [Create a gRPC request](/docs/sending-requests/grpc/grpc-request-interface/) and [Invoke a gRPC request](/docs/sending-requests/grpc/first-grpc-request/).

Once you've created your gRPC requests, you can learn about testing them in [Test and debug values in gRPC requests using JavaScript in Postman](/docs/sending-requests/grpc/scripting-in-grpc-request/) and [Write tests for gRPC requests using JavaScript assertions in Postman](/docs/sending-requests/grpc/test-examples/).

Simulating gRPC services is a valuable tool for testing and development. Learn more in [Create and use gRPC mock servers](/docs/sending-requests/grpc/using-grpc-mock/).
