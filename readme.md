# Stock Market Simulator Server Manager

The **Stock Market Simulator Server Manager** is a powerful tool designed to facilitate the management of stock market infomration and user information for use in [**Stock Market Simulator Client**](https://github.com/Robby-Sodhi/stock-market-simulator-client) for educational purposes. It provides an intuitive graphical interface for administrators or owners of these servers to efficiently oversee and control various aspects of the simulator, including student performance, server configuration, and real-time stock data retrieval. This server manager is designed with the flexibility to support multiple servers on a single network, making it ideal for educators who wish to host their own servers to monitor their specific classrooms of students.

**Java Library for Server Interaction**

A Java library that simplifies the process of discovering, connecting to, and interacting with the Stock Market Simulator Server. This library streamlines the client-side experience, allowing you to seamlessly integrate your applications with the server manager. This is used in the [**Stock Market Simulator Client**](https://github.com/Robby-Sodhi/stock-market-simulator-client) and can be used to build clients for a wide range of devices.

Features of the Java Library:

Server Discovery: Discover available servers on the network effortlessly using SSDP (Simple Service Discovery Protocol).

Connection Management: Establish and manage connections to the server, ensuring a reliable and efficient user experience.

Data Communication: Easily communicate with the FastAPI REST API on the server, enabling you to retrieve user information, stock data, and more.

Usage Examples

To help you get started with the Java library, we've included detailed usage examples in the provided folder. These examples will guide you through the process of integrating the library into your Java applications, making it easier than ever to interact with the Stock Market Simulator Server.

## Key Components

The Stock Market Simulator Server Manager comprises three main components, each serving a unique purpose:

High-level diagram of server components:

**![](https://lh7-us.googleusercontent.com/j6RLbcpNQhFSFYIiBEGyx3lIhO6UubW9TYw0lIjivw9WW_QmPFBgM1p37ALpZXsGe5ysGsqPYreaSaN9-04LdHD08Lir8nAsRxqXyjuy4BYG6CqFDXNcyfbqfmB7XXhHK4MjPaiphTGLJk1zR1Yf-1E)**

### 1. SSDP Server (Simple Service Discovery Protocol)

The SSDP server is responsible for broadcasting the existence of the stock market simulator server on the network. It provides essential information such as the server's ownership, location (IP address and port), and other relevant details. This component enables clients to discover available servers efficiently, making it easy for students and administrators to find and connect to the desired simulator server.

### 2. Unicorn ASGI (Asynchronous Server Gateway Interface)

Unicorn ASGI serves as the asynchronous server that hosts and manages connections to the FastAPI REST API.

### 3. FastAPI REST API

The FastAPI REST API acts as the core of the server manager, facilitating data communication between the server and clients. It offers a range of functionalities, including user information requests, stock data retrieval, and configuration options. Additionally, it connects to the relevant Yahoo finance APIs to fetch real-time stock data, ensuring that the simulator remains up-to-date and responsive.

## Data Storage

User data in the Stock Market Simulator Server Manager is stored in a SQLite database, providing a reliable and lightweight solution for managing user accounts, performance records, and other related information. To optimize data retrieval and prevent rate limiting issues, the server caches certain stock information, updating it only as needed. This approach helps reduce the time required for requests, ensuring that the simulator operates smoothly and efficiently.

## Getting Started

To get started with the Stock Market Simulator Server Manager, please refer to the documentation and installation instructions provided in the project page.

## Contact

If you have questions, feedback, or require assistance, please reach out to rsodhi@uwaterloo.ca

## references

[UPnP Device Architecture 2.0](https://openconnectivity.org/upnp-specs/UPnP-arch-DeviceArchitecture-v2.0-20200417.pdf)
