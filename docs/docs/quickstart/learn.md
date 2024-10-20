# Quick Start Guide to EIPI

EIPI is a Domain-Specific Language (DSL) for building and managing APIs with minimal code. Designed for simplicity, EIPI enables developers to define API behavior using structured configuration files. It abstracts the complexities of routing, request handling, and payload processing, making API creation feel natural and fast.

## 1. What Makes EIPI Special?

EIPI functions like a framework but with the elegance of a DSL. Instead of writing boilerplate code, you describe the API's behavior using configuration files. This encourages declarative programming, allowing you to focus on what the API should do rather than how to implement it.

- **Declarative Syntax:** Define API endpoints, methods, payloads, and responses through configuration files.
- **Environment-Aware:** Secure secrets and configurations with environment variables.
- **Dynamic Routes:** Routes are generated automatically from configuration files.

## 2. How Does EIPI Work?

EIPI reads `.eipi` files to understand the structure and behavior of the APIs. These files contain instructions like HTTP methods, routes, payloads, and responses, which EIPI translates into working endpoints.

Example `.eipi` Configuration:

```eipi
    /*
    *  Creating our first API endpoint using Eipi
    */

    [
        {
            "name": "Just an API Endpoint",
            "description": "Demonstrating API using Eipi",
            "method": "GET",
            "route": "/api/v1",
            "response": {
                "status": 200,
                "body": {
                    "text": "Your hitting an API end point"
                }
            }
        }
    ]
```

This configuration will automatically generate a `/api/v1` endpoint that returns the "response" highlighted on the codes

## 3. Handling Environment Variables

Sensitive information, such as API keys, is stored in `.env.eipi` files to keep them secure. EIPI reads these variables dynamically during runtime.

Example `.env.eipi`:

```env
MY_ENV_VARIABLE=your_actual_env_variable
```

In the .eipi configuration, you can refer to this value using {{ env_WEATHER_API_KEY }}.

## 4. Routing and API Management Made Easy

With EIPI, each route is automatically mapped based on the configuration provided. You don’t need to write any routing logic. EIPI ensures that your API is ready to handle requests with minimal setup.

## 5. Declarative Payloads and Responses

The payload section describes external actions the API should take (like calling another API). EIPI allows you to define responses directly in the configuration, making API design seamless.

## Why EIPI?

EIPI simplifies API management, especially for projects that require fast prototyping or involve multiple microservices. By combining the principles of a DSL with the flexibility of a framework, EIPI allows developers to:

- Rapidly build APIs with a focus on configuration over code.
- Manage external calls and responses effortlessly.
- Keep secrets secure with environment variable support.

---

With EIPI, building APIs becomes intuitive and declarative making development faster, cleaner, and more enjoyable.
