# AI Image Metadata Extractor

A simple, client-side web tool to extract and view generation metadata from AI-generated PNG images. Just drag and drop an image to see its prompt, negative prompt, and other generation parameters.

This tool runs entirely in your browser. No images are uploaded to any server.

## ✨ Features

-   **Drag & Drop Interface**: Easily drag and drop an image file to analyze it.
-   **Multiple Formats Supported**: Extracts data from images created with:
    -   Stable Diffusion WebUI (A1111)
    -   ComfyUI
    -   Fooocus
    -   NovelAI
    -   And more...
-   **Formatted & Raw Views**: View metadata in a clean, human-readable format or as raw JSON data.
-   **Easy Copying**:
    -   Copy the positive and negative prompts with a single click.
    -   Copy all generation parameters in a WebUI-compatible format.
-   **Client-Side Processing**: All processing is done in your browser for complete privacy.
-   **Clean & Responsive UI**: A minimalist, Shadcn-inspired design that works great on both desktop and mobile devices.

## 🚀 How to Use

1.  **Open the File**: Simply open the `index.html` file in any modern web browser (like Chrome, Firefox, or Safari).
2.  **Upload an Image**:
    -   Drag and drop a PNG image file into the upload area.
    -   Or, click the upload area to select an image file from your computer.
3.  **View Metadata**:
    -   The extracted metadata will be displayed automatically.
    -   Switch between the **Formatted** and **Raw JSON** tabs to see the data in different views.
4.  **Copy Data**:
    -   Use the `Copy` buttons next to the prompt fields to copy them individually.
    -   Use the `Copy All Parameters` button to copy the complete generation data to your clipboard.

## 🛠️ Technical Details

-   **Frontend**: Built with vanilla HTML, CSS, and JavaScript. No frameworks are required.
-   **Metadata Parsing**: The script reads PNG `tEXt`, `iTXt`, and `zTXt` chunks directly from the file buffer.
-   **Decompression**: Uses the `pako.js` library to decompress zlib-compressed metadata chunks commonly used by ComfyUI.