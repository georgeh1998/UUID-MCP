# UUID-MCP (Submodule)

A simple UUID generator service implemented using the Model Context Protocol (MCP) Kotlin SDK.

## Overview

This service runs an MCP-compliant server that generates and returns random UUIDs upon request. When a client connects via the MCP protocol, the server generates a new UUID and returns it as a string.

## Implementation Details

The service follows the Model Context Protocol (MCP), a lightweight protocol designed for AI model/client communication:

- Uses the MCP Kotlin SDK version 0.4.0
- Provides a handler named "uuid" that generates random UUIDs
- Uses the StdioServerTransport for communication

## Building and Running

### Prerequisites

- JDK 17 or later
- Gradle

### Build

```bash
./gradlew build
```

### Run the Server

```bash
./gradlew run
```

This will start the server using stdio as the transport mechanism.

## Example Output

When a client connects and calls the "uuid" handler, the server generates and returns a UUID:

```
INFO  com.github.george1998h.uuidmcp.MainKt - Generated UUID: 550e8400-e29b-41d4-a716-446655440000
```

## Notes

- Uses `java.util.UUID.randomUUID().toString()` for UUID generation
- Implements logging for server operations
- Follows MCP protocol specifications
