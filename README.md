# Proxy Server with Cache

A multi-threaded HTTP proxy server implemented in C that caches web content using the Least Recently Used (LRU) policy to improve performance and reduce redundant network calls.

## Features

- 🧵 **Multi-threading:** Handles multiple client requests concurrently using threads.
- 🔒 **Thread Synchronization:** Implements semaphores to ensure safe access to shared resources.
- 📦 **Caching Mechanism:** Efficient LRU cache implementation to serve repeated requests quickly.
- 🔗 **HTTP Request Forwarding:** Acts as an intermediary between client and web server, forwarding and caching GET requests.
- 🛠️ **Robust Design:** Handles invalid requests, caching logic, and concurrency with stability.

## Technologies Used

- C Programming Language  
- Threads
- Semaphores  
- TCP/IP Sockets  
- LRU Cache Design  
- Makefile for build automation  

## How It Works

1. Client sends an HTTP GET request to the proxy server.
2. Proxy checks the cache:
   - If present: sends cached response.
   - If not: forwards the request to the original server, caches the response, and returns it to the client.
3. Handles multiple clients simultaneously using multi-threading.
4. Uses semaphores to ensure mutual exclusion when accessing or modifying shared resources like the cache.

