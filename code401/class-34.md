# React 4

## Next.js - Dynamic Routes

Dynamic routes

Next.js enables you to define dynamic routes in your app using the brackets ([param]). Instead of setting a static name on your pages, you can use a dynamic one.

Let's use this folder structure as an example:

```tree
    ├── pages
    |  ├── index.js
    |  ├── [slug].js
    |  └── my-folder
    |     ├── [id].js
    |     └── index.js
```

Next.js will get the route parameters passed in and then use it as a name for the route.

- index.js

```jsx
export default function IndexPage() {
  return (
    <ul>
      <li>
        <Link href="/">
          <a>Home</a>
        </Link>
      </li>
      <li>
        <Link href="/[slug]" as="/my-slug">
          <a>First Route</a>
        </Link>
      </li>
      <li>
        <Link href="/my-folder/[id]" as="/my-folder/my-id">
          <a>Second Route</a>
        </Link>
      </li>
    </ul>
  )
}
```

Here, we have to define the value on the as attribute because the path is dynamic. The name of the route will be whatever you set on the as prop.

- [slug].js

```jsx
import { useRouter } from "next/router"

export default function DynamicPage() {
  const router = useRouter()
  const {
    query: { id },
  } = router
  return <div>The dynamic route is {id}</div>
}
```

You can get the route parameters as well with the useRouter hook on the client or getInitialProps on the server.

- my-folder/[id].js

```jsx
export default function MyDynamicPage({ example }) {
  return <div>My example is {example}</div>
}

MyDynamicPage.getInitialProps = ({ query: { example } }) => {
  return { example }
}
```

Here, we use getInitialProps to get the dynamic route passed in.

## Next.js - Deployment

Deploy to Vercel

The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database. We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. You can start using it for free — no credit card required.