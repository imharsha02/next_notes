# next_notes

### create next application
```javascript
npx create-next-app <appName>
```

### Add new pages
Inside the pages directory, add a new file with '.js' extension. This will help in file based routing as well

### Dynamic routes
Inside a folder in the pages directory, 
create a file, like, [pathVariable].js
Inside the file,
```javascript
import {useRouter} from 'next/router'
const router = useRouter();
const pathVariable = router.query.pathVariable
```
The path variable in the code and the path variable in the file name are the same
