# Blazor in .NET 8: Introduction

https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-8.0

Blazor is a component based **SPA(Single Page Application)** that achieves interactiviy with C#

Blazor is a framework that allows us to create interactive applications that will be used, mainly, though a web browser

See also this video in youtube: https://www.youtube.com/watch?v=gq1ySblcyA8

![image](https://github.com/luiscoco/Blazor_video1/assets/32194879/27ce5b9f-874e-4a04-be45-eaca8dc9d896)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/a82bf67c-7882-44e4-83ea-52d16adc43e9)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/7234887d-db0e-4841-9939-2271cabee388)

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

Here's a breakdown of the key differences between Blazor WebAssembly and Blazor Server-Side, along with guidance on choosing the right model:

**Blazor WebAssembly (WASM)**

How it works: Your C# Blazor components run directly in the user's web browser using a WebAssembly-based .NET runtime

The entire app (its components, .NET dependencies, and runtime) is downloaded to the browser at startup

**Pros**:

Offline capabilities: Apps can work even without an active network connection (if designed appropriately)

Reduced server load: The client's browser handles most of the processing

Leverage client resources: Access client-specific hardware or browser APIs if required

**Cons**:

Larger download size: Initial download can be slower, especially on less powerful devices or limited networks

Performance limitations: May perform less optimally compared to Blazor Server for highly CPU-intensive tasks, due to the constraints of WebAssembly execution

.NET compatibility: Not every .NET API is available in the WebAssembly environment

**Blazor Server-Side**

How it works: Your Blazor components run entirely on the server. User interactions and UI updates are sent over a real-time SignalR connection between client and server

**Pros**:

Faster initial load: Smaller download size means the app appears faster in the browser

Full .NET access: Full access to all .NET APIs available on the server

Simplified development (sometimes): No need to consider offline scenarios

Thinner clients: Great for users with older devices or less-powerful browsers

**Cons**:

Scalability demands: Increased server-side load as the number of users grows

Dependency on network: A constantly active network connection is essential for the app to work

Higher latency: UI updates might feel slightly less snappy compared to WebAssembly due to network roundtrips

**When to Choose Which**

Consider these factors when deciding between WASM and Server-Side:

Offline support: If offline capabilities are crucial, Blazor WebAssembly is the way to go

Performance needs: For raw computational speed and very frequent UI updates, Blazor Server-Side often has an edge

Deployment complexity: Blazor Server-Side apps are generally simpler to deploy

Security: Blazor Server-Side may be slightly more secure, as your app logic does not leave the server

Development resources: Do your developers have strong C#/.NET skills? Both are C#-based, but debugging Blazor WebAssembly can sometimes be trickier

**Additional Considerations**

Blazor Hybrid: This model gives you the flexibility to mix WASM and Server components

Project evolution: Be aware that technology is evolving quickly; the differences between these models might narrow over time

## 7. First Blazor samples

https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-tutorial/intro

https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-cli-tutorial/modify

## 8. Blazor project templates in Visual Studio 2022 Community Edition

- **Blazor Web App**: a project template for creating a Blazor web app that supports both server-side rendering and client interactively. This template can be used for web apps with rich dynamic user interfaces (UIs).
    
- **Blazor WebAssembly Standalone App**: a project template for creating a Blazor app than runs on WebAssembly. This template can be used for web apps with rich dynamic user interfaces (UIs).

- **Blazor WebAssembly App Empty**: an empty template for creating a Blazor app than runs on WebAssembly and is optionally hosted by an ASP.NET Core app. This template does not have any content in it.

- **Blazor Server App**: a project template for creating a Blazor server app that runs server-side inside an ASP.NET Core app and handles user interactions over a SignalR connection. This template can be used for web apps with rich dynamic user interfaces (UIs).
  
- **Blazor Server App Empty**: an empty project template for creating a Blazor server app that runs server-side inside an ASP.NET Core app and handles user interactions over a SignalR connection. This template does not have any content in it.

### 8.1. Template 1 (Blazor Web App)

https://www.youtube.com/watch?v=kbvdnUTZ_xA&t=4s

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/b4f86f75-b55d-4452-8717-d0d0d2851ae6)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/ab6812e9-1c41-44ae-b7de-3003dae94cbb)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/c019511d-cdfe-4cab-a1bb-f7a82113c807)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/b584949d-2b57-4b1d-ac9d-368109205db5)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/c9198d89-ff78-4f2c-8a3f-7e4ab0942116)

This is the application middleware(program.cs)

**program.cs**

```csharp
using BlazorApp1.Components;

var builder = WebApplication.CreateBuilder(args);

// Add services to the container.
builder.Services.AddRazorComponents()
    .AddInteractiveServerComponents();

var app = builder.Build();

// Configure the HTTP request pipeline.
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Error", createScopeForErrors: true);
    app.UseHsts();
}

app.UseHttpsRedirection();

app.UseStaticFiles();
app.UseAntiforgery();

app.MapRazorComponents<App>()
    .AddInteractiveServerRenderMode();

app.Run();
```

The **App.razor** page is invoked from the application middleware(program.cs):

**App.razor**

```razor
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <base href="/" />
    <link rel="stylesheet" href="bootstrap/bootstrap.min.css" />
    <link rel="stylesheet" href="app.css" />
    <link rel="stylesheet" href="BlazorApp1.styles.css" />
    <link rel="icon" type="image/png" href="favicon.png" />
    <HeadOutlet />
</head>

<body>
    <Routes />
    <script src="_framework/blazor.web.js"></script>
</body>

</html>
```

The **Routes.razor** file is invoked with the **Routes** tag defined inside the **App.razor** page

```razor
<Router AppAssembly="typeof(Program).Assembly">
    <Found Context="routeData">
        <RouteView RouteData="routeData" DefaultLayout="typeof(Layout.MainLayout)" />
        <FocusOnNavigate RouteData="routeData" Selector="h1" />
    </Found>
</Router>
```

The Routes.razor established as DefaultLayout the **MainLayout.razor** file

This is the **MainLayout.razor** page content

This page contains two main tags: 

- The navigation component (**NavMenu**). This component shows the menu option in the left hand side window

- The **@Body** tag, for rendering the pages content in the **MainLayout** page

**MainLayout.razor**

```razor
@inherits LayoutComponentBase

<div class="page">
    <div class="sidebar">
        <NavMenu />
    </div>

    <main>
        <div class="top-row px-4">
            <a href="https://learn.microsoft.com/aspnet/core/" target="_blank">About</a>
        </div>

        <article class="content px-4">
            @Body
        </article>
    </main>
</div>

<div id="blazor-error-ui">
    An unhandled error has occurred.
    <a href="" class="reload">Reload</a>
    <a class="dismiss">🗙</a>
</div>
```

The navigation component (**NavMenu**), see the menu options in the following code

```razor
<div class="top-row ps-3 navbar navbar-dark">
    <div class="container-fluid">
        <a class="navbar-brand" href="">BlazorApp1</a>
    </div>
</div>

<input type="checkbox" title="Navigation menu" class="navbar-toggler" />

<div class="nav-scrollable" onclick="document.querySelector('.navbar-toggler').click()">
    <nav class="flex-column">
        <div class="nav-item px-3">
            <NavLink class="nav-link" href="" Match="NavLinkMatch.All">
                <span class="bi bi-house-door-fill-nav-menu" aria-hidden="true"></span> Home
            </NavLink>
        </div>

        <div class="nav-item px-3">
            <NavLink class="nav-link" href="counter">
                <span class="bi bi-plus-square-fill-nav-menu" aria-hidden="true"></span> Counter
            </NavLink>
        </div>

        <div class="nav-item px-3">
            <NavLink class="nav-link" href="weather">
                <span class="bi bi-list-nested-nav-menu" aria-hidden="true"></span> Weather
            </NavLink>
        </div>
    </nav>
</div>
```


### 8.2. Template 2 (Blazor WebAssembly Standalone App)



### 8.3. Template 3 (Blazor WebAssembly App Empty)



### 8.4. Template 4 (Blazor Server App)



### 8.5. Template 5 (Blazor Server App Empty)




## 9. Blazor project templates in VSCode

https://www.youtube.com/watch?v=aVkddRsOx1w&t=21s

We can list the blazor CLI templates with the following command:

```
dotnet new list
```

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/9ce15a83-a574-4ebc-9306-b7ec485549d2)

For example we can create a new blazor apps with the following commands:

```
dotnet new blazorserver
```

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/03f8dca3-a367-4d47-9189-0e3166b3aaad)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/68e4b76d-08d8-4f93-8884-eadc66b3e2d4)

![image](https://github.com/luiscoco/Blazor_in_.NET-8_Introduction/assets/32194879/3cae3271-f3c6-4cb3-ab20-22fb9c546eb3)



