# Blazor in .NET 8: Introduction

https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-8.0

Blazor is a component based **SPA(Single Page Application)** that achieves interactiviy with C#

Blazor is a framework that allows us to create interactive applications that will be used, mainly, though a web browser

See also this video in youtube: https://www.youtube.com/watch?v=gq1ySblcyA8

![image](https://github.com/luiscoco/Blazor_video1/assets/32194879/27ce5b9f-874e-4a04-be45-eaca8dc9d896)

## 1. What is Blazor?

Blazor is a powerful web framework from Microsoft that lets you build interactive web applications using C# instead of relying solely on JavaScript:

**C# Everywhere**: If you know C#, you can build both the frontend (what the user sees) and backend (server-side logic) of your web applications

**Component-Based Architecture**: Similar to modern JavaScript frameworks like React or Vue, Blazor uses components as building blocks. These components encapsulate UI elements, logic, and reusability

**Flexibility**: Blazor offers two main flavors:

**Blazor Server**: Your components run on the server, and UI updates are sent to the browser over a real-time connection (SignalR). Excellent for fast initial page load and real-time applications

**Blazor WebAssembly (WASM)**: Your components run directly in the browser using WebAssembly (a low-level, high-performance code format). Great for offline capabilities and reducing server load

**.NET 8 Enhancements**

**Static Server-Side Rendering (SSR)**: Render your Blazor components into static HTML on the server for lightning-fast first-page loads and improved SEO

**Streaming Rendering**: Start sending HTML to the browser before the entire page is fully rendered, resulting in quicker perceived loading times

**Enhanced Navigation and Forms**: More control over navigation and form handling

**Auto Mode Interactivity**: Components can intelligently switch between Blazor Server and Blazor WebAssembly based on specific needs

## 2. Essential Blazor Capabilities

**Component-Based Architecture**: Building modular, reusable UI blocks:

- Basic components

- Parameter passing

- Event handling

**Routing**: Navigation and deep-linking within your Blazor application

**Forms and Validation**: Creating forms, input binding, and validating user input

**Data Binding**: Synchronizing component state with data

**Templating**: Providing flexible layouts and content structures for components

**Dependency Injection**: Injecting services and components

## 3. More Advanced Blazor Capabilities

**JavaScript Interop**: Calling JavaScript functions from C# and vice versa

**State Management**: Managing data and its flow across different components

**Error Handling and Boundaries**: Gracefully handling exceptions and providing fallback UI

**Authentication and Authorization**: Securing routes, components, and managing user permissions

**Offline Capabilities**: Building Blazor WebAssembly applications that function even when the device is offline

**Custom Rendering**: Fine-grained control over how components render their output (useful for specialized UI elements)

**Server-Side Rendering (SSR)**: Pre-rendering components on the server for improved SEO and first-load performance

-------------------------------------------------------------------------------------------------------------------------------------

**Additional Samples and Areas to Explore** (still PENDING)

**Dependency Injection (advanced)**: Complex service injection scenarios, configuring DI containers

**State Management (advanced)**: Using dedicated state management libraries like Redux or Fluxor

**Component Libraries**: Integrating third-party Blazor component libraries for rich UI elements

**Server-Side Rendering (SSR)**: Detailed examples of setting up SSR in Blazor apps

**Blazor WebAssembly Performance Optimization**: Profiling and techniques to improve Blazor Wasm performance

**Blazor Testing**: Unit and integration testing of Blazor components

-------------------------------------------------------------------------------------------------------------------------------------

## 4. Blazor Web Assembly

We can use WebAssembly to execute .NET apps in a web browser

Blazor (client-side)

Blazor (client-side + ASP.NET Core)

We run .NET Core in the browser

We need WebAssembly

Advantage: highly scalable

Disadvantage: Downloading the .NET runtime + DLLs

## 5. Blazor Server-Side

The Blazor application runs on the server, and the user interacts with it through a SignalR connection

Advantage: Devices with less resources should be able to run the application without problems

Blazor server-side limitations relate to the server

1 vCPU - 3.5 Gb of memory handles over 5000 users concurrently

4 vCPU - 14 Gb of memory handles over 20000 users concurrently

Disadvantage: latency 

## 6. Hosting models

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/2557158f-6aa8-4dc7-b736-7716ae5dfa9d)

## 7. First Blazor samples

https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-tutorial/intro

https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-cli-tutorial/modify

## 8. Blazor project templates in Visual Studio 2022 Community Edition

- **Blazor Web App**: a project template for creating a Blazor web app that supports both server-side rendering and client interactively. This template can be used for web apps with rich dynamic user interfaces (UIs).
    
- **Blazor WebAssembly Standalone App**: a project template for creating a Blazor app than runs on WebAssembly. This template can be used for web apps with rich dynamic user interfaces (UIs).

- **Blazor WebAssembly App Empty**: an empty template for creating a Blazor app than runs on WebAssembly and is optionally hosted by an ASP.NET Core app. This template does not have any content in it.

- **Blazor Server App**: a project template for creating a Blazor server app that runs server-side inside an ASP.NET Core app and handles user interactions over a SignalR connection. This template can be used for web apps with rich dynamic user interfaces (UIs).
  
- **Blazor Server App Empty**: an empty project template for creating a Blazor server app that runs server-side inside an ASP.NET Core app and handles user interactions over a SignalR connection. This template does not have any content in it.

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/d1573c98-2126-4411-8e6b-695c75a05de6)



## 9. Blazor project templates in VSCode



