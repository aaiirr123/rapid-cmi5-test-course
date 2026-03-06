# Using Git

Storing courses in **Git** enables collaboration using one of the most powerful and widely adopted version control systems available.

By managing course content in Git, authors can:

* **Collaborate with other authors** using familiar workflows such as branching, pull requests, and code reviews.
* **Track every change** made to a course over time with a complete version history.
* **Easily roll back** to previous versions if mistakes are made or content needs to be restored.
* **Audit changes** to understand who modified content and why.
* **Integrate with DevOps and automation platforms** such as GitHub and GitLab for validation, publishing, and deployment workflows.

Rapid CMI5 stores courses as **human-readable Markdown along with all associated assets** directly in your repository.
This means your course content remains:

* **Transparent** – easily readable and editable
* **Portable** – not locked into a proprietary format
* **Fully owned by you** – stored in infrastructure you control

By keeping your course content in Git, you gain the reliability, collaboration, and automation capabilities that modern software development teams rely on.

# Configuring Git

Rapid CMI5 allows you to configure a **global Git profile** so you can easily interact with your course repositories.

To configure Git:

1. Click the **gear icon** in the **top-right corner** of the application.
2. Select **"Configure Git"** from the menu.
3. Enter your:
   * **Author Name** – Your full name
   * **Author Email** – The email associated with your Git account

These values will be used when creating commits so that changes to course content are properly attributed.

***

## Creating a Personal Access Token (PAT)

To authenticate with remote Git repositories, you will need to create a **Personal Access Token (PAT)** for your Git account.

When creating the token:

* Grant **only the minimum permissions required**
* Typically this means **read and write access to repositories**

After generating the PAT:

1. Copy the token from your Git provider (e.g., GitHub or GitLab).
2. Return to the **Git Configuration** screen in Rapid CMI5.
3. Paste the token into the **PAT / Access Token** field.

Once configured, Rapid CMI5 can securely interact with your repositories, allowing you to:

* **Clone repositories**
* **Commit changes**
* **Push updates**
* **Pull the latest course content**

This setup enables seamless version control and collaboration directly within the authoring tool.