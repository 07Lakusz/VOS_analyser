[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.16759348.svg)](https://doi.org/10.5281/zenodo.16759348)
# VOS_Analyser
# Automated Network Analysis Report Generator

This project provides Python-based tools, designed for Google Colab, that automate the process of bibliometric analyses, specifically network analysis and generate a comprehensive, multi-page PDF report. It is specifically tailored to process data exported from VOSviewer, but can be adapted for other network data sources.
For now, as a proof of concept, the keyword analyser is implemented and ready to be used in your bibliometric research.

## Key Features

-   **Automated Data Processing:** Loads and validates node and edge CSV files via the pandas package.
-   **Comprehensive Network Analysis:** Calculates multiple centrality metrics (Degree, Betweenness, Closeness, Eigenvector), cluster coherence, influential keyword analysis and temporal trends with the networkx package.
-   **Dynamic PDF Report Generation:** Uses the `reportlab` library to create a multi-page PDF analysis report with text, tables, and visualisations.
-   **Interactive Colab UI:** A simple, guided workflow allows users to upload files, trigger the analysis, download the report, and clean up the environment with distinct button clicks.
-   **Error Handling:** The workflow includes validation checks and automatic cleanup of files upon error to ensure a clean state.

## Installation Guide

1.  **Download the Notebook:** Download the `.ipynb` file from this repository to your local computer.
2.  **Upload to Google Colab:**
    *   Go to [Google Colab](https://colab.research.google.com/).
    *   In the welcome pop-up, click on the **"Upload"** tab.
    *   Drag and drop the `.ipynb` file you just downloaded.
3.  **Save a Copy:** Once the notebook is open, go to `File > Save a copy in Drive`. This will save a permanent, editable copy to your own Google Drive. You can now close the original and work from your saved version.

## How to Use

This project is designed to be run as a Google Colab notebook (`.ipynb`).

1.  **Setup:** Open the notebook in Google Colab. The first cell will install the necessary libraries.
2.  **Configuration:** The second cell contains a `config` dictionary where you can adjust parameters like PDF titles and data column names to match your specific files. The remaining cells configure the analysis and PDF generation functions.
3.  **Run the Workflow:** Execute the final cell (labelled "EXECUTION"). This will initiate the interactive workflow:
    a. A file upload dialogue will appear. Select your `_node.csv`, `_edge.csv`, and visualisation (`.png`) files.
    b. After a successful upload, a **"Start Analysis"** button will appear. Click it to begin processing.
    c. Once the analysis is complete, a **"Download Report"** button will be displayed. Click it to download the generated PDF.
    d. After initiating the download, a **"Clean Up Files"** button will become active. Click it to remove all uploaded files and the generated report from the Colab session.

## Technology Stack

-   **Language:** Python 3
-   **Environment:** Google Colab
-   **Core Libraries:**
    -   `pandas` for data manipulation.
    -   `networkx` for graph analysis.
    -   `reportlab` for PDF generation.
    -   `ipywidgets` for the interactive UI in Colab.

## How to Cite

If you use this software-code in your research, please cite it. This project is archived on Zenodo and has a permanent Digital Object Identifier (DOI).

A `CITATION.cff` file is also included in this repository for easy import into most citation management tools (e.g., Zotero, Mendeley, EndNote).

### APA 7 Style

Juhász, L. P. (2025). VOS_analyser (Version 0.1.0) [Computer software]. Zenodo. https://doi.org/10.5281/zenodo.16759347

### BibTeX

@software{juhasz_2025_16759347,
  author       = {Juhász, L. P.},
  title        = {VOS_analyser},
  version      = {0.1.0},
  publisher    = {Zenodo},
  year         = {2025},
  doi          = {10.5281/zenodo.16759347},
  url          = {https://doi.org/10.5281/zenodo.16759347}
}

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
