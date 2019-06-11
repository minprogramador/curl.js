# curl.js


### exemplos
```

const Curl = require('./Curl');

const run = async function () {

	const curl = new Curl();
	let url = 'https://httpbin.org/post';
	let proxy = '';

	curl.setUrl(url);
	//curl.setProxy(proxy);
	curl.setCookie("ping=pong");
	//console.log(curl.getCookie());
	curl.setRef('https://www.google.com');
	// console.log(curl.getRef());
	curl.setPost({username: 'admin', pass: 'root'});
	curl.setHeaders({'User-Agent': 'curl'});
//	let d = curl.getOpts();
//	console.log(d);
	// let a = curl.getConfig();
	// console.log(a);

	let xx = await curl.run();
	console.log(xx.body);

};

run();


```