# Astro Setup v1

This repository provides a pre-configured setup for an Astro project, integrated with Tailwind CSS for styling and Cypress for end-to-end testing. Below is a detailed guide to help you get started and customize your project further.

## Features

- **Astro Framework**: A modern, lightweight framework for building static sites.
- **Tailwind CSS**: Utility-first CSS framework for rapid UI development.
- **Cypress**: End-to-end testing framework to ensure your application functions as expected.
- **Extensibility**: Easily add support for React or Vue components.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/hasanh47/astro-setup-v1.git
   cd astro-setup-v1
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

   Your application will be available at `http://localhost:4321`.

## Tailwind CSS Integration

Tailwind CSS is pre-installed and configured for this setup. You can find the configuration file at `tailwind.config.js`.

## Adding Framework Support

### React

To integrate React components into your Astro project:

1. Install the React integration:

   ```bash
   npx astro add react
   ```

2. Import and use React components in your `.astro` files:

   ```astro
   ---
   import MyReactComponent from "../components/MyReactComponent.jsx";
   ---

   <MyReactComponent />
   ```

### Vue

To integrate Vue components into your Astro project:

1. Install the Vue integration:

   ```bash
   npx astro add vue
   ```

2. Import and use Vue components in your `.astro` files:

   ```astro
   ---
   import MyVueComponent from "../components/MyVueComponent.vue";
   ---

   <MyVueComponent />
   ```

## Cypress Testing Incoming

Cypress is configured for end-to-end testing. Test files are located in the `cypress/e2e/` directory.

### Running Tests

1. Start the development server:

   ```bash
   npm run dev
   ```

2. Open the Cypress test runner:

   ```bash
   npx cypress open
   ```

3. Run your tests from the test runner interface.

### Writing Tests

Create new test files in the `cypress/e2e/` directory. Here's an example test:

```typescript
// cypress/e2e/index.cy.ts
it("titles are correct", () => {
  const page = cy.visit("http://localhost:4321");

  page.get("title").should("have.text", "Astro is awesome!");
  page.get("h1").should("have.text", "Hello world from Astro");
});

```

## Additional Scripts

- `npm run build`: Build the project for production.
- `npm run preview`: Preview the production build.
- `npm run test`: Run all Cypress tests in headless mode.

## Project Structure

```
astro-setup-v1/
├── public/            # Static assets
├── src/
│   ├── components/    # Astro/React/Vue components
│   ├── layouts/       # Layout components
│   ├── pages/         # Astro pages
│   └── assets/        # Static assets
├── cypress/
│   ├── e2e/          # End-to-end tests
├── tailwind.config.js # Tailwind CSS configuration
└── package.json       # Project dependencies and scripts
```

## Contribution

Feel free to fork this repository, make your changes, and submit a pull request. Contributions are welcome!

---

Enjoy building with Astro Setup v1!
