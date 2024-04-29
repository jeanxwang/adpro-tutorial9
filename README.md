# Tutorial 9 - Reflection

## Aliyah Faza Qinthara (2206024726)

### What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?

- **Unary RPC**: This type of RPC consists of a one-time request and response between a client and a server, ideal for straightforward interactions where a client’s request is met with a single server reply.
- **Server Streaming RPC**: This RPC model allows a server to send multiple responses to a client following a single request, fitting for use cases like delivering a series of data, such as transaction logs.
- **Bidirectional Streaming RPC**: In this model, both client and server exchange messages back and forth, making it perfect for interactive applications like messaging platforms that require ongoing communication.

### What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?

When deploying gRPC services with Rust, it’s crucial to consider security aspects like user verification, access control, and encrypted data transfer. Techniques like TLS, JWT, and authorization middleware can be employed to secure client-server exchanges.

### What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?

Managing bidirectional streaming in Rust’s gRPC for applications like chat services can present obstacles, including handling simultaneous streams, maintaining message sequence, addressing errors smoothly, and applying backpressure strategies to avoid overloading either end.

### What are the advantages and disadvantages of using the `tokio_stream::wrappers::ReceiverStream` for streaming responses in Rust gRPC services?

The `ReceiverStream` from the `tokio_stream::wrappers` module is a handy tool for turning a `tokio::sync::mpsc::Receiver` into a stream that works with Tokio’s asynchronous environment, offering ease of use and integration with the Tokio framework, though it might lack the versatility of bespoke stream solutions.

### In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?

Enhancing code flexibility and modular design in Rust gRPC applications can be achieved by organizing code into modules, defining interfaces for services, applying dependency injection, and using design principles like dependency inversion to separate components.

### In the **MyPaymentService** implementation, what additional steps might be necessary to handle more complex payment processing logic?

For intricate payment processing in `MyPaymentService`, steps could include verifying transaction details, interfacing with payment systems, managing exceptional cases such as retries and errors, and setting up logging and surveillance for transaction tracking.

### What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?

Integrating gRPC as a communication standard can reshape the structure and strategy of distributed networks by facilitating swift and effective microservice interactions, accommodating various coding languages, and offering functionalities like data streaming and automatic code creation.

### What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?

HTTP/2, the foundation of gRPC, brings benefits like concurrent data streams, reduced header size, and server-initiated data transfer, which are not present in HTTP/1.1. Nonetheless, it could add complexity and extra load in comparison to HTTP/1.1 or WebSocket for basic RESTful services, depending on specific needs and system setup.

### How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?

While REST APIs’ request-response pattern is well-suited for basic interactions, it falls short for real-time exchanges. gRPC’s bidirectional streaming excels in scenarios requiring instant communication, such as chat apps.

### What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?

The structured protocol of gRPC, using Protocol Buffers, provides benefits like precise type definition, schema checking, and more efficient data encoding than REST’s JSON. However, it might necessitate more tools and system support for managing schemas and could be less adaptable in certain situations.
