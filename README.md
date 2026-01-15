# blogging-site-django
A simple blogging site built with Django

## Django Request–Response Cycle

Django follows a structured flow to process HTTP requests and return responses.

### Request Flow

1. **Client Request**
   - A user requests a page by entering a URL in a web browser.
   - The web server forwards the HTTP request to Django.

2. **URL Routing**
   - Django checks the requested URL against the URL patterns defined in `urls.py`.
   - It stops at the first pattern that matches the request.

3. **View Execution**
   - Django calls the view function or class associated with the matched URL.
   - The view contains the business logic for handling the request.

4. **Model Interaction (Optional)**
   - The view may interact with models to retrieve or modify data.
   - Models define the structure of data and handle database queries.

5. **Template Rendering**
   - The view renders a template (usually HTML) using the retrieved data.
   - Django returns the rendered template as an HTTP response.

### Models
- Define database structure and relationships.
- Provide methods for querying and manipulating data.
- Act as the interface between the application and the database.

### Middleware (Important but Hidden Layer)

Middleware is a powerful but often invisible part of Django’s request–response cycle.

- Middleware sits **between the incoming HTTP request and the outgoing HTTP response**.
- It can **modify requests before the view is executed**.
- It can **modify responses before they are sent back to the client**.
- Common uses of middleware include:
  - Authentication
  - Security
  - Session management
  - Logging
  - Request/response preprocessing

Middleware is intentionally not shown in basic diagrams to keep the request–response flow simple.  
You will learn more about Django’s built-in middleware and how to create **custom middleware** in later chapters.
