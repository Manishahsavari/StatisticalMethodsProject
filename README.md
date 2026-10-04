# Statistical Methods Project

A university statistical analysis project focused on **production analysis, data preprocessing, statistical methods, and analytical reporting**. The project includes a Python-based analysis application, a preprocessed dataset, presentation materials, and the resources required to build and run the application.

## Overview

This project was developed as part of a university **Statistical Methods** course/project.

The repository combines:

* A Python-based production analysis application
* Preprocessed statistical data
* Application/build configuration
* PDF presentation and architecture documentation
* Supporting resources for PDF generation
* Project documentation and requirements

The project is structured to keep source code, data, executable-generation resources, and presentation materials separated.

---

## Project Structure

```text
StatisticalMethodsProject/
│
├── Codes_Documents/
│   ├── Document.json
│   ├── ProductionAnalyzer_Modern.py
│   ├── R.jpg
│   ├── requirements.txt
│   └── weasyprint/
│       ├── LICENSE
│       ├── README.rst
│       └── dist/
│           └── weasyprint.exe
│
├── ExecutableProgramSource/
│   └── ProductionAnalyzer_Modern.spec
│
├── PreProcessedDataSet/
│   └── DataSet.xlsx
│
├── PresentationFiles/
│   ├── Essential.mp4
│   ├── Presentation.pdf
│   └── ProgramArchitecture.pdf
│
└── .gitignore
```

### `Codes_Documents/`

Contains the main project source and supporting resources.

**`ProductionAnalyzer_Modern.py`**
The main Python application implementing the project's production-analysis functionality and graphical user interface.

The application also includes a PDF export component that uses **WeasyPrint** to convert generated HTML content into PDF documents.

**`Document.json`**
Project-related JSON documentation/configuration.

**`requirements.txt`**
Python dependencies required by the application.

**`R.jpg`**
Supporting project resource.

### `ExecutableProgramSource/`

Contains the PyInstaller specification used to build the application executable:

```text
ProductionAnalyzer_Modern.spec
```

Generated `build/` and `dist/` directories are intentionally excluded from version control.

### `PreProcessedDataSet/`

Contains the processed dataset used by the project:

```text
DataSet.xlsx
```

### `PresentationFiles/`

Contains the project's presentation and supporting materials:

* `Presentation.pdf` — project presentation
* `ProgramArchitecture.pdf` — application architecture documentation
* `Essential.mp4` — supplementary presentation material

---

## Technologies

The project primarily uses:

* **Python**
* **Tkinter** for the graphical user interface
* **Pandas / data-processing tools** for working with structured data
* **WeasyPrint** for PDF generation
* **PyInstaller** for packaging the application as a standalone executable
* **JSON / Excel** for project data and documentation

> The exact Python dependencies are listed in `Codes_Documents/requirements.txt`.

---

## Application

The main application is implemented in:

```text
Codes_Documents/ProductionAnalyzer_Modern.py
```

The application provides a graphical interface for working with the project's production-analysis workflow.

One of its implemented components is a PDF export system. The application locates and invokes `weasyprint.exe` to generate PDF output from HTML content.

The interface also provides functionality for configuring the WeasyPrint executable path when necessary.

---

## Data

The project uses a preprocessed Excel dataset:

```text
PreProcessedDataSet/DataSet.xlsx
```

The dataset is kept separately from the application source code to make the project structure easier to understand and maintain.

---

## Building the Application

The project includes a PyInstaller specification:

```text
ExecutableProgramSource/ProductionAnalyzer_Modern.spec
```

PyInstaller can be used to generate a standalone executable from the Python application.

Generated build artifacts such as:

```text
build/
dist/
```

are excluded from Git through `.gitignore`.

This keeps the repository focused on **source code and reproducible project resources rather than generated build artifacts**.

---

## Running the Project

Clone the repository:

```bash
git clone https://github.com/Manishahsavari/StatisticalMethodsProject.git
cd StatisticalMethodsProject
```

Create a Python virtual environment:

```bash
python3 -m venv venv
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

On Windows:

```powershell
venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r Codes_Documents/requirements.txt
```

Then run the main application:

```bash
python Codes_Documents/ProductionAnalyzer_Modern.py
```

### WeasyPrint

The PDF export functionality requires the WeasyPrint executable configured by the application.

The repository includes the project's bundled Windows executable under:

```text
Codes_Documents/weasyprint/dist/weasyprint.exe
```

The application also provides a mechanism to manually select the executable path if it is not detected automatically.

---

## Documentation

Additional project documentation is available in the repository:

### Presentation

`PresentationFiles/Presentation.pdf`

Contains the main project presentation.

### Program Architecture

`PresentationFiles/ProgramArchitecture.pdf`

Provides documentation of the application's architecture and organization.

---

## Repository Design

The repository follows a simple separation of concerns:

```text
Source Code
     │
     ├── ProductionAnalyzer_Modern.py
     │
     ▼
Data
     │
     └── DataSet.xlsx
     │
     ▼
Analysis / Application
     │
     ├── GUI
     ├── Production Analysis
     └── PDF Export
     │
     ▼
Documentation & Presentation
     │
     ├── Presentation.pdf
     └── ProgramArchitecture.pdf
     │
     ▼
Executable Build
     │
     └── PyInstaller specification
```

This structure separates the application source, data, documentation, and executable-generation resources while keeping the repository reproducible and maintainable.

---

## Contributors

This project was developed collaboratively as a university project.

**Mohammad Shahinfar**
Statistics / Data Science

**Manish Ahsavari**

For details about individual contributions, see the repository's Git history and GitHub contributor information.

---

## Academic Context

This project was developed as part of a university **Statistical Methods** project and demonstrates the integration of:

* Statistical data analysis
* Data preprocessing
* Python programming
* Application development
* Data visualization/reporting
* Automated document generation
* Software packaging

---

## License

See the repository's `LICENSE` file for licensing information.
