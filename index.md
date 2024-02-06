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
    </style>
</head>
<body>

<nav>
    <a href="http://127.0.0.1:4100/frontcasts/signup">Signup</a>
    <a href="http://127.0.0.1:4100/frontcasts/edit">Edit</a>
    <a href="http://127.0.0.1:4100/frontcasts/data">Data</a>
</nav>

<!-- Your page content goes here -->

</body>
</html>

