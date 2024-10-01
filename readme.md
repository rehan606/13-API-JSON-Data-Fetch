
<h1 align="center"> Display JSON user data when Button click </h1>





# Display JSON user data when Button click


```js
    function userData(data){
        const apiUr = 'https://jsonplaceholder.typicode.com/users'
        fetch(apiUr)
        .then(response => response.json())
        .then(data => displayUsers(data))
    }

    function displayUsers(data){
        const usrList = document.getElementById('user-list')
        for(const user of data){
            const li = document.createElement('li')
            li.innerText = user.name
                
            usrList.appendChild(li)
        }
    }

```


# Display Load Post API Data


```js

    function loadPost(){
        fetch('https://jsonplaceholder.typicode.com/posts')
        .then(response => response.json())
        .then(data => displayPost(data) )
    }


    function displayPost(data){
        const allPost = document.getElementById('post-data')
        for (const post of data){
            const div = document.createElement('div')
            
            div.innerHTML = `
                <h4 class="">id: ${post.id} </h4>
                <p class="text-blue-800">Title: ${post.title} </p>
                <p class="">Body: ${post.body} </p>
            `
            allPost.appendChild(div)
        }
    }

    loadPost()
```




