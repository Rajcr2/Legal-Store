# Legal-Store

An end-to-end **UiPath RPA automation** that scrapes, resolves, and downloads official Bare Acts PDFs from public legal portals by intelligently navigating multi-step web flows.

This project automates the complete workflow from **index page → handle pages → bitstream PDF downloads**, while handling duplicates, dynamic content, and clean file naming.

### Key Features

1. **Automated Bare Acts Scraping** for extracting official laws listings.
2. **Dynamic Handle URL Resolution** to navigate IndiaCode intermediary various Act pages.
3. **PDF (Bitstream) Extraction** by resolving multi-level redirects.
4. **End-to-End PDF Download Automation** using UiPath's HTTP Request activity.
5. **Duplicate-Safe Execution** through file-existence checks.
6. **Production-Ready UiPath Workflow Design**

### Objectives

The primary goal of this automation is to :

1. Create an automated data collection pipeline to support a **RAG-based Legal Advisor Chatbot**, where manually sourcing and maintaining legal Act PDFs is not practical.
2. Automate the process of downloading a large number of official Indian legal Act PDFs using **UiPath RPA**, thereby reducing manual effort and time consumption.
3. Handle the complete navigation flow from the Bare Acts listing page to IndiaCode handle pages and finally to the actual law PDF links in a reliable and repeatable manner.
4. Store downloaded legal documents in a structured and maintainable format using meaningful, human-readable, and OS-safe filenames.
5. Ensure that the automation is scalable and reliable by incorporating de-duplication, logging, and basic error-handling mechanisms as the number of legal Acts increases.

### Prerequisites

#### Software

- **UiPath Studio (Windows)** – This project is built entirely using UiPath Studio as a no-code / low-code RPA solution.
- **Windows OS** – Required for UiPath Studio and Windows-based automation.

#### UiPath Dependencies

Install the following packages via Manage Packages in UiPath Studio:

- **UiPath.System.Activities (v25.10.3)** – Core workflow logic, control flow, file operations, and logging.
- **UiPath.UIAutomation.Activities (v25.10.21)** – Browser automation, web navigation, and dynamic data extraction.
- **UiPath.WebAPI.Activities (v2.3.2)** – HTTP/API handling and final PDF URL resolution.

### Workflow Architecture

**Phase 1 – Collect Handle URLs**
1. Open Bare Acts index page
2. Locate and filter valid Act links
3. Extract href values
4. Store unique handle URLs in collection

**Phase 2 – Resolve PDFs & Download**
1. Loop through each handle URL
2. Navigate to IndiaCode page
3. Locate PDF section
4. Extract:
   - Law name
   - Bitstream PDF link
5. Sanitize law name
6. Download PDF using HTTP Request
7. Save to local directory


### Output



https://github.com/user-attachments/assets/632b8e7d-e515-42c3-8600-6b5be5ad2006


### Conclusion

**Legal-Store** successfully automates the end-to-end collection of official Indian legal Act PDFs, replacing a time-consuming manual process with a reliable **UiPath RPA workflow**. This automation also provides a scalable data foundation for my RAG-based Legal Advisor Chatbot and other legal analytics systems.



