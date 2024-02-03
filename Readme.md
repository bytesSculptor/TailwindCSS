# Steps to setup Tailwind CSS in a plain HTML and CSS project

**Step 1: Install Tailwind CSS**
```bash
npm install -D tailwindcss
npx tailwindcss init
```

**Step 2: Create your HTML and CSS files**
Create `index.html` and `style.css` files in your project folder.

**Step 3: Configure your template paths (Optional)**
Open `tailwind.config.js` and add the paths to your template files if you have them in a specific folder. If not, you can skip this step.

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./**/*.html"], // Add this line if you have a specific folder structure
  theme: {
    extend: {},
  },
  plugins: [],
}
```

**Step 4: Add the Tailwind directives to your CSS**
Open your `style.css` file and add the Tailwind directives:

```css
/* style.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

**Step 5: Start the Tailwind CLI build process**
Run the following command in your terminal to build your CSS file:

```bash
npx tailwindcss -i style.css -o output.css --watch
```

This command watches for changes in your `style.css` file and outputs the compiled CSS to `output.css`.

**Step 6: Link the compiled CSS in your HTML**
Open your `index.html` file and link the compiled CSS file in the `<head>` section:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="output.css" rel="stylesheet">
  <title>Your Tailwind CSS Project</title>
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

**Step 7: Start using Tailwind in your HTML**
Now, you can use Tailwind CSS utility classes in your HTML to style your content. In the example above, `text-3xl`, `font-bold`, and `underline` classes are used in the `<h1>` element.

That's it! You've simplified the process for setting up Tailwind CSS in a plain HTML and CSS project.