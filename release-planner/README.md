## **Release Planner 🚀**


<p align="center">
    <img src="./Single_mainlogo_tm.png" alt="Release Planner Icon"  height="100%">
</p>

### **Overview**  
The **Release Planner** is a streamlined application designed to help teams efficiently manage software releases. It provides structured access to repositories, release notes, and version tags, ensuring smooth coordination across multiple products.

### **Features**  
✅ **Interactive Release Planning** – Intuitive form-based interface for creating comprehensive release plans  
✅ **Project Details Management** – Configure application name, version, milestone, release dates, and priorities  
✅ **Release Components Management** – Add, edit, and remove multiple service release components  
✅ **Multiple Export Formats** – Export projects as JSON, CSV, or PDF files  
✅ **JSON Import/Export** – Full project portability with drag-and-drop JSON upload support  
✅ **Interactive Tables** – Visual release management with responsive table views  
✅ **Priority Management** – Set release priorities (Critical, High, Low) with visual indicators  
✅ **Repository Integration** – Link to GitHub repositories and deployment packages  
✅ **Deployment Version URLs** – Support for Docker Registry and Helm Chart version references  
✅ **Rich Text Editing** – Detailed descriptions and notes for each release component  
✅ **Modern UI/UX** – Beautiful responsive design with gradient overlays and smooth animations  
✅ **Live Component Counter** – Real-time display of configured release components  
✅ **Form Validation** – Required field validation and data integrity checks  
✅ **Clear All Functionality** – One-click form reset for starting new release plans  
✅ **Branding & Social Impact** – Social responsibility messaging and community contribution guidance  
✅ **Mobile Responsive** – Optimized for all device sizes and screen orientations

---
👉 [Visit the Release Planner](https://open-source.releasepilot.com/release-planner)

---

## **Usage** 📌  

### **Getting Started**
1. **Set Up Project Details** – Fill in application name, version, milestone name, release date, priority level, and description
2. **Configure Release Components** – Click "Add Component" to start adding release services with repository links, tags, and deployment URLs
3. **Manage Components** – Edit or remove components using the action buttons in the component table
4. **Export Your Plan** – Use any of the export options (JSON, CSV, PDF) to save or share your release plan

### **Adding Release Components**
1. **Click "Add Component"** to open the component dialog
2. **Fill Required Fields**: Service Name, Repository Link, Tag (at minimum)
3. **Add Optional Details**: Release documents, descriptions, notes, deployment version URLs
4. **Save Component** and it will appear in your release plan table

### **Export Options**
- **📥 Download JSON** – Save your complete project configuration for sharing or backup
- **📊 Export CSV** – Generate spreadsheet-compatible data for analysis and collaboration  
- **📄 Export PDF** – Create printable release plan summaries with full project details
- **🔄 Clear All** – Reset the form to start a new release plan

### **Import Data**
1. **Upload JSON** – Drag and drop JSON files directly onto the upload area, or click to browse
2. **Automatic Population** – All form fields will be populated from the imported data
3. **Drag & Drop Interface** – Visual drag-and-drop zone with hover effects and file validation
4. **Validation** – Invalid JSON files will show appropriate error messages with guidance

### **Interactive UI Components**
- **Gradient Design** – Beautiful visual interface with modern card-based layouts
- **Component Table** – Organized tabular view with service names, repositories, tags, and deployment URLs
- **Form Dialogs** – Modal-based component editing with full form controls
- **Responsive Tables** – View all components in an organized table format
- **Live Component Counter** – See real-time count of configured components
- **Priority Indicators** – Visual priority labels (🚨 Critical, ⚡ High, 📋 Low)
- **Component Management** – Inline edit and delete functionality for each component
- **Form Validation** – Real-time validation ensures data quality
- **Real-time Updates** – Live component counting and instant UI updates
- **Responsive Layout** – Optimized for desktop, tablet, and mobile devices
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

### **How to Use Data Formats in the App**  

#### **JSON Format (Primary)**
1️⃣ Populate the planner interactively using the form fields.  
2️⃣ Click "📥 Download JSON" to export the current plan as a `.json` file.  
3️⃣ Click "⬆️ Upload JSON" to import an existing `.json` file and auto-populate the form.  
4️⃣ Ensure each release has at least: **name, repo_link, tag**. Optional: **note, description, deployment_version_url, release_document**.

#### **CSV Export**
5️⃣ Click "📊 Export CSV" to generate spreadsheet format with all release components  
6️⃣ CSV includes columns: Service Name, Repository Link, Tag, Release Document, Note, Description, Deployment Version URL

#### **PDF Export** 
7️⃣ Click "📄 Export PDF" to generate a printable report with project overview and all release details  
8️⃣ PDF includes formatted project information, priority levels, and detailed component listings

#### **Supported Requirements**
- **Required Fields**: Service name, repository link, tag
- **Optional Fields**: Release document, note, description, deployment version URL  
- **Validation**: All uploads are validated for proper JSON format and required fields

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
