# React 3A

## Assets

Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets.

## Metadata

Metadata is to modify the metadata of the page

- Example: Changing the < title> HTML tag

1. Find the following lines:

```html
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```

2.import: ```import Head from 'next/head'```

- Result:

```jsx
import Head from 'next/head'
export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
    </>
  )
}

```

## CSS

Writing and Importing CSS

Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.

Using popular CSS libraries like Tailwind CSS is also supported.

## What is React context?

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.

When should you use React context?

React context is great when you are passing data that can be used in any component in your application.

These types of data include:

- Theme data (like dark or light mode)
- User data (the currently authenticated user)
- Location-specific data (like user language or locale)

Data should be placed on React context that does not need to be updated often.

Why? Because context was not made as an entire state management system. It was made to make consuming data easier.
