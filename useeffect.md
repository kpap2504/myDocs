React Hook useEffect to fetch data from local json file to create a details page

```js
import React, { useEffect, useState } from "react"

export default function Example() {
	const [posts, setPosts] = useState([])

	useEffect(() => {
		fetch("https://jsonplaceholder.typicode.com/posts")
			.then((response) => response.json())
			.then((data) => {
				setPosts(data) 
			})
	}, [])

	return (
		<div>
			<h1>Cool app</h1>
			{posts.map((item) => (
				<li>
					<h2>{item.title}</h2>
					<p>{item.description}</p>
				</li>
			))}
		</div>
	)
}
```



https://rahmanfadhil.com/fetch-data-with-react-hooks/

https://dev.to/antdp425/react-fetch-data-from-api-with-useeffect-27le

https://alexkondov.com/an-ode-to-effects/




