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
✅ **JSON Download** – Export the full plan as a pretty-printed `.json` file.  
✅ **JSON Upload** – Import a `.json` file to populate the entire form.

---
👉 [Visit the Release Planner](https://open-source.releasepilot.com/release-planner)

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

| Field                           | Type     | Description |
|---------------------------------|---------|-------------|
| `name`                          | String  | The name of the application. |
| `version`                       | String  | The current release version of the planner. |
| `description`                   | String  | A brief overview of the application. |
| `milestone_name`                | String  | Milestone name for the release cycle. |
| `release_date`                  | String  | Target release date (YYYY-MM-DD). |
| `priority`                      | String  | Priority of the release (`critical`, `high`, `low`). |
| `releases`                      | Array   | A list of service releases. |
| `releases[].name`               | String  | The name of the service being released. |
| `releases[].repo_link`          | String  | URL of the GitHub repository. |
| `releases[].tag`                | String  | The version tag associated with the release. |
| `releases[].release_document`   | String  | Link to the release document. |
| `releases[].note`               | String  | Any additional notes for the service release. |
| `releases[].description`        | String  | Description of the service release. |
| `releases[].deployment_version_url` | String | Link to deployment package or chart version. |

---

### **Example JSON Data**  

```json
{
  "name": "Release Planner",
  "version": "R1.0",
  "description": "Track and manage your software releases efficiently.",
  "milestone_name": "M1",
  "release_date": "2025-09-30",
  "priority": "high",
  "releases": [
    {
      "name": "Service A",
      "repo_link": "http://github.com/users",
      "tag": "v1.0.0",
      "release_document": "http://example.com/document.pdf",
      "note": "Roll out in wave-1",
      "description": "Core authentication service",
      "deployment_version_url": "https://registry.example.com/auth/chart/1.0.0"
    },
    {
      "name": "Service B",
      "repo_link": "http://github.com/repo/service-b",
      "tag": "v2.1.0",
      "release_document": "http://example.com/service-b-doc.pdf",
      "note": "Depends on Service A",
      "description": "Payments service",
      "deployment_version_url": "https://ghcr.io/org/payments:2.1.0"
    }
  ]
}
```

---

### **How to Use JSON Data in the App**  


1️⃣ Populate the planner interactively using the form fields.  
2️⃣ Click "📥 Download Release Plan" to export the current plan as a `.json` file.  
3️⃣ Click "⬆️ Upload JSON" to import an existing `.json` file and auto-populate the form.  
4️⃣ Ensure each release has at least: **name, repo_link, tag, release_document**. Optional: **note, description, deployment_version_url**.  

---

This documentation ensures that anyone using the project understands the JSON structure and can modify it as needed. 🚀 Let me know if you want any refinements! 😊

## **Contributing** 🤝  

💡 Contributions are welcome! Feel free to:  
- **Report bugs** via GitHub Issues  
- **Suggest features** or improvements  


## **License** 📜  
This project is licensed under the **MIT License**.  

---

## 💛 Donate Back – Not Just Money
If Release Pilot boosted your productivity by 0.1%—give back through impact, not money 🌟

🤝 Help others
👥 Mentor fellow developer
🚀 Share opportunities
💡 Contribute skills
❤️ Spread kindness
Every small action matters. Let your gratitude become someone else's breakthrough. 🙌

*Made with ❤️ as part of the Release Pilot Toolbox* 
### **Made with ❤️ from India 🇮🇳**  
