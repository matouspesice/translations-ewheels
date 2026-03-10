# 🚴 E-Bike Questions Editor

A lightweight, browser-based JSON editor designed specifically for managing e-bike configuration questions and answer logic. This tool allows users to upload a JSON schema, edit question titles and answer definitions in real-time, and export the modified data while preserving the original file structure.

---

## ### Key Features

* **Drag-and-Drop Upload:** Quickly load your `.json` configuration files.
* **In-Place Editing:** Click any text field (titles, names, or bucket definitions) to edit instantly.
* **Structural Integrity:** Automatically preserves additional JSON fields like `parameters` that aren't directly edited.
* **Smart Search:** Filter through dozens of questions and answers by keyword to find specific logic blocks.
* **Validation:** Includes basic JSON schema validation to ensure the file contains the required `questions` array.
* **One-Click Export:** Download your changes as a formatted JSON file with an `-edited` suffix.

---

## ### Getting Started

### 1. Requirements

Since this is a standalone HTML file using CDN-delivered React and Tailwind CSS, there is **no installation** required. You only need a modern web browser.

### 2. Usage

1. Open the `index.html` file in your browser.
2. Drag your questions JSON file into the upload zone (or click to browse).
3. Expand question cards to see associated answers.
4. Click on any text to enter **Edit Mode**.
* Press `Enter` to save (or the green checkmark).
* Press `Escape` to cancel (or the red "X").


5. Click **Export JSON** to save your changes to your device.

---

## ### Expected JSON Structure

The editor expects a JSON format similar to the following:

```json
{
  "parameters": [], 
  "questions": [
    {
      "code": "unique-q-code",
      "title": "What is your primary use case?",
      "answers": [
        {
          "code": "ans-001",
          "name": "Commuting",
          "bucketDefinition": "score_city += 10"
        }
      ]
    }
  ]
}

```

---

## ### Technical Stack

* **React 18:** Functional components and hooks for state management.
* **Tailwind CSS:** For a clean, responsive, and "app-like" UI.
* **Babel Standalone:** Enables JSX processing directly in the browser.
* **Lucide-inspired SVGs:** Lightweight iconography for navigation.

> **Note:** This tool runs entirely client-side. Your data never leaves your browser and is not uploaded to any server.

Would you like me to add instructions on how to extend the editor for new data fields?
