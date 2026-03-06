# Desktop vs Web Application

Rapid CMI5 is available in two versions:

1. **Desktop Application**
2. **Web Application**

***

## Web Application

### Pros

* **No installation required** — users can access the editor directly in a browser.
* **Built-in SSO configuration** — authentication and access to the Range Engine are already integrated.

### Drawbacks

* **CORS limitations** restrict how the application can interact with external Git repositories.
* Users **cannot directly push to many public Git hosting services** (such as GitHub) unless those services are configured to allow the requests.
* Typically requires a **self-hosted Git server** configured to allow Rapid CMI5 requests.

***

## Desktop Application

### Pros

* **Better performance**, allowing the editor to handle **larger and more complex courses**.
* **No CORS restrictions**, enabling direct interaction with Git repositories and other services.
* Can **push to public Git providers** such as GitHub, GitLab, or internal repositories without special server configuration.
* Allows **custom certificate configuration** for air-gapped or internal environments.

### Drawbacks

* Requires **downloading and installing** a separate application.
* **SSO must be configured manually** during setup.