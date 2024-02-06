---
layout: home
search_exclude: true
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navigation Bar</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        nav {
            background-color: #333;
            overflow: hidden;
        }
        nav button {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        nav a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        nav a:hover {
            background-color: #ddd;
            color: black;
        }

        nav a.active {
            background-color: #4CAF50;
            color: white;
        }
            nav button:hover {
            background-color: #ddd;
            color: black;
        }

        nav button.active {
            background-color: #4CAF50;
            color: white;
        }
    </style>
</head>
<body>

<nav>
    <a href="http://127.0.0.1:4100/frontcasts/signup">Signup</a>
    <a href="http://127.0.0.1:4100/frontcasts/edit">Edit</a>
    <a href="http://127.0.0.1:4100/frontcasts/data">Data</a>
    <button onclick = "eraseCookie()">Logout </button>
</nav>

<!-- Your page content goes here -->

</body>
</html>

<script>
    function eraseCookie() {   
        document.cookie = 'jwt=; Max-Age=0; path=/; domain=' + location.hostname;
        console.log(document.cookie) 
        window.location.reload()
}
    let options = {
        method: 'GET',
        headers: {
            'Content-Type': 'application/json;charset=utf-8'
        },
        credentials: 'include'
    }
    function getCookie(name) {
    var match = document.cookie.match(RegExp('(?:^|;\\s*)' + name + '=([^;]*)')); 
    return match ? match[1] : null;
}
    addEventListener("load", (event) => {
        console.log(getCookie("jwt"))
        if(getCookie("jwt")){
            return
        }
        else {
            window.location.href = "http://127.0.0.1:4100/frontcasts/login.html"
        }
    })