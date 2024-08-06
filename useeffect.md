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


05/08/2024
https://dev.to/srijan_karki/the-proper-use-of-useeffect-in-react-a-comprehensive-guide-1edi
```js
// Fetching Data on Component Mount
 useEffect(() => {
     const fetchData = async () => {
       const result = await fetch('https://api.example.com/data');
       const data = await result.json();
       setData(data);
     };
     fetchData();
   }, []); // Empty dependency array ensures this runs only once on mount
```   

```js   
// Setting Up Intervals or Subscriptions   
 useEffect(() => {
     const intervalId = setInterval(() => {
       console.log('Interval running');
     }, 1000);
     return () => clearInterval(intervalId); // Cleanup on unmount
   }, []);   
```   
   

