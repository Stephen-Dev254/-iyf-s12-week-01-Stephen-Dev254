# Task 1.2: DevTools Exploration

## Website 1: https://example.com

### 1. What HTML tags are used on the page?
The page uses a minimal, clean set of structural and content elements:
- `<!DOCTYPE html>`
- `<html>`
- `<head>` (containing `<title>`, `<meta charset>`, `<meta name="viewport">`, and `<style>`)
- `<body>`
- `<div>` (used as a structural container layout card)
- `<h1>` (the primary heading element)
- `<p>` (text paragraph blocks)
- `<a>` (the hyperlink pointing to additional domain information)

### 2. What is the page title?
The explicit page title found inside the `<title>` tag in the document `<head>` is:
**Example Domain**

### 3. How many headings are there?
There is exactly **1 heading** present on the entire page:
- An `<h1>` element containing the text content "Example Domain".

---

## Website 2: https://mozilla.org

### 1. Find the navigation menu - what tag is it wrapped in?
The core top-level navigation layout container is explicitly wrapped using the semantic HTML **`<nav>`** element (with a class or id identifying it as the header navigation menu block).

### 2. How is the search bar structured?
The search bar interface components follow standard form controls:
- It is nested inside a container (often a `<form>` element configured for search).
- It features an `<input>` element with `type="search"`, an explicit `id` hook, a descriptive `placeholder` property ("Search..."), and accompanying search parameters.
- It includes layout icon elements representing a search magnifying glass and an explicit clear button wrapper.

### 3. What happens when you hover over links (check the styles)?
When interacting with hyperlinks via interactive hover state pseudo-classes (`a:hover`):
- The `text-decoration` attribute changes dynamically (e.g., shifts from `none` to an active `underline` effect).
- The text color value updates to an active state accent color (such as a deeper blue or purple theme accent) to establish explicit interactive focus.

---

## Website 3: Custom Choice (GitHub Homepage)

### 1. Identify 5 different HTML elements
- `<header>`: Used to wrap the global layout navigation architecture.
- `<main>`: Contains the unique primary body blocks of the webpage.
- `<section>`: Separates the layout into structural topic modules.
- `<button>`: Represents interactive clickable command points or menu triggers.
- `<ul>`: Groups unordered list points together for item listings.

### 2. Find a form element and list its inputs
The "Sign up for GitHub" user entry form module handles these explicit inputs:
- `<input type="email">`: Collects user signup email parameters securely.
- `<input type="hidden">`: Submits hidden layout validation or cross-site request tokens behind the scenes.

### 3. Elements Panel Screenshot
*(Remember to capture a crop showing your opened browser DevTools Elements panel view, place the image file inside your `images/` directory, and link it below).*

![Elements Panel Review](images/devtools-elements-panel.png)
