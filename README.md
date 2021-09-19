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
const {params[]} = router.query // destructuring the params and storing the returned content in the 'params' array

Perform desaired operation on the array
```
