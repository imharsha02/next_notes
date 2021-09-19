# next_notes

### create next application
```javascript
npx create-next-app <appName>
```

### Add new pages
Inside the pages directory, add a new file with '.js' extension. This will help in file based routing as well

### Dynamic routes
Inside a folder in the pages directory.
create a file: [pathVariable].js in that directory.
Inside the file,
```javascript
import {useRouter} from 'next/router'
const router = useRouter();
const pathVariable = router.query.pathVariable
```
The path variable in the code and the path variable in the file name are the same


### Catch all routes
Inside the folder for dynamic routes inside the pages directory, create a file: [...params].js. Inside that file,
```javascript
import {useRouter} from 'next/router
const router=useRouter();
const {params=[]} = router.query // destructuring the params and storing the returned content in the 'params' array

Perform desaired operation on the array
```

### Navigation between pages from client side
```javascript
import Link from 'next/link'
...
<Link href="<path to visit>"><a><clickable text></a></Link>
```

### Navigating to dynamic routes
```javascript
<Link href=`folderName/prop`><a>Clickable text</a></Link>
```
The prop in the href of Link component is the formal parameter passed into the functional component

### replace attribute
Replaces the entair history back to the root home page insted of adding new route
```javascript
<Link href="<path to navigate>" replace><a><clickable text></a></Link>
```

### Navigate bsed on event
```javascript
import {useRouter} from 'next/router'
export default function (){
...
const router= useRouter();
function handleClick(){
router.push("<pathToRedirect>")
}
return (
<Link href = "<path to redirect>"><button onClick = {handleClick}>button</button></Link>
)
}
```
