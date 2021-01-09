# next_notes

### Create a next.js project:
```javascript
npx create-next-app project_name
```

### To create a new page:
Inside the pages folder, create a new file with '.js' extension

### To link two pages:
```javascript
import Link from 'next/link'
...
...
...
<Link href="path of the file"><a>link Name</a></Link> (OR) <Link href="path of the file"><button>Button name</button></Link>
```

### Static assets:
Static assets like images must be inside the public folder (which is at the top level)
## To use the image
```javascript
<img src="/imgName.extension" alt="alternate text if image does not render"/>
```

### Manipulate meta data (head part of the page)
```javascript
import Head from 'next/head'
<Head>
<title>page title</title>
</Head>
```

### layout for the application:
1) Create a top level components folder.
2) Now create a layout.js file inside the components folder.
3) Inside this file, create a defaultly exported function which returns all the layout tag's children components in a div like this:
```javascript
export default function Layout(){
  return (
    <div>{children}</div>
  )
}
```

### applying the layout to the application
inside the components inside the pages folder,
```javascript
import Layout from '../../components/layout.js'
export default function pageName(){
  <Layout>
  ...
  </Layout>
}
```

### defining styles to the Layout:
1) Inside the components folder, create a layout.module.css file
2) Inside this file, define wanted styles.
3) Then, inside the layout.js file (present in the components folder),
```javascript
import styles from './layout.module.css'
export default function Layout(children){
return (
<div className={styles.container}>{children}</div>
)
}
```
Note: The name of the class while assigning to jsx element must be styles.<className> because we are importing 'styles' from the file which has the module.css extension
  
  ### Global styles to the app
  the _app.js file in the pages folder provides the functionality specified in it to the entair application
  The .css file can be created anywhere, but to apply the styles globally, import that file in the _app.js file only.
  That is done by writing the following code in the _app.js file
  ```javascript
  import '../styles/global.css'

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}

```
  
