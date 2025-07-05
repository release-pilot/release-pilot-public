## **Release Planner 🚀**


<p align="center">
    <img src="./Single_mainlogo_tm.png" alt="Release Planner Icon"  height="100%">
</p>

### **Overview**  
The **Release Planner** is a streamlined application designed to help teams efficiently manage software releases. It provides structured access to repositories, release notes, and version tags, ensuring smooth coordination across multiple products.

### **Features**  
✅ **Release Tracking** – Displays key release details, including repository links and version tags.  
✅ **Documentation Access** – Quick access to release documents for seamless communication.  
✅ **Interactive Dialog** – Provides additional release information in a modal popup.  
✅ **Branding & Aesthetics** – Includes a centered brand logo, descriptive headlines, and a footer message: _"Made with love from India ❤️🇮🇳"._  

---
👉 [Visit the Release Planner](https://app.releasepilot.com/release-planner)

---

## **Usage** 📌  

1. **View Release Information**  
   - Each release displays a **name, tag version, and links** to the repository and release document.  
   - Icons provide quick access to relevant resources.  

2. **Get More Details**  
   - Click the ℹ️ (info) icon to open a **dialog box** with a brief about the release planner.  

---
## **JSON Data Structure 📄**  

The **Release Planner** application uses a structured JSON format to store and display release information. Below is the data schema and an example of how to use it.

### **Schema Definition**  

| Field              | Type     | Description |
|--------------------|---------|-------------|
| `name`            | String  | The name of the application. |
| `version`         | String  | The current release version of the planner. |
| `description`     | String  | A brief overview of the application. |
| `releases`        | Array   | A list of service releases. |
| `releases[].name` | String  | The name of the service being released. |
| `releases[].repo_link` | String | URL of the GitHub repository. |
| `releases[].tag`  | String  | The version tag associated with the release. |
| `releases[].release_document` | String | Link to the release document. |

---

### **Example JSON Data**  

```json
{
    "name": "Release Planner",
    "version": "R1.0",
    "description": "Track and manage your software releases efficiently.",
    "releases": [
        {
            "name": "Service A",
            "repo_link": "http://github.com/users",
            "tag": "v1.0.0",
            "release_document": "http://example.com/document.pdf"
        },
        {
            "name": "Service B",
            "repo_link": "http://github.com/repo/service-b",
            "tag": "v2.1.0",
            "release_document": "http://example.com/service-b-doc.pdf"
        }
    ]
}
```

---

### **How to Use JSON Data in the App**  


1️⃣ Add new services by expanding the `releases` array.

3️⃣ Ensure that each release has a **name, repo_link, version tag,** and **release document** for proper display in the UI.

---

This documentation ensures that anyone using the project understands the JSON structure and can modify it as needed. 🚀 Let me know if you want any refinements! 😊

## **Contributing** 🤝  

💡 Contributions are welcome! Feel free to:  
- **Report bugs** via GitHub Issues  
- **Suggest features** or improvements  


## **License** 📜  
This project is licensed under the **MIT License**.  

---


*Made with ❤️ as part of the Release Pilot Toolbox* 
### **Made with ❤️ from India 🇮🇳**  
