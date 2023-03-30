# api-project

- https://randomuser.me/ is a website that provides dummy data for random users that we can easily work with. We can get the response by making a request to https://randomuser.me/api/
- we will recieve a JSON resposefor this 

- script.js contains the code that will make the API request and handle the response

- the async/await function, ensures that the data is displayed even after the page is loaded

## Notes  

# Async
- Async: It simply allows us to write promises-based code as if it was synchronous and it checks that we are not breaking the execution thread. It operates asynchronously via the event loop. Async functions will always return a value. It makes sure that a promise is returned and if it is not returned then JavaScript automatically wraps it in a promise which is resolved with its value.

- example 1 (shows the basic use of async in Javascript): 
    const getData = async() => {
    var data = "Hello World";
    return data;
    }
      
    getData().then(data => console.log(data));

output: Hello World

# Await
- Await: Await function is used to wait for the promise. It could be used within the async block only. It makes the code wait until the promise returns a result. It only makes the async block wait.

- example 2 (shows the basic use of the await keyword in Javascript):
	const getData = async() => {
		var y = await "Hello World";
		console.log(y);
	}
	
	console.log(1);
	getData();
	console.log(2);

output: 1
        2
        Hello World

- console prints 2 before the “Hello World”, this is due to the usage of the await keyword