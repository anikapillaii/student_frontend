<html       >
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<div class="form-container">
    <form>
        <input type="text" id="name" class="input" placeholder="Full Name"><br>
        <input type="text" id="user" class="input" placeholder="Username"><br>
        <input type="password" id="pass" class="input" placeholder="Password">
    </form>
        <button class = "submit" onclick = "signup()">Log In</button>
        <p id = "error"></p>
</div>
<script>
function signup() {
    data = {
        "name": document.getElementById("name").value,
        "uid": document.getElementById("user").value,
        "password": document.getElementById("pass").value
    }
    let options = {
    method: 'POST',
    headers: {
        'Content-Type':
            'application/json;charset=utf-8'
    },
    body: JSON.stringify(data)
}
    let sign_up = fetch('http://127.0.0.1:8086/api/users/authenticate', options);
    sign_up.then(response => {
        if (response.status === 200) {
            console.log('All Cookies:', document.cookie);
            document.getElementById("error").innerHTML = ""
    // Print out the cookie and the response data
            console.log(document.cookie)
            // Check if the JWT cookie is present
            //window.location.href = "http://127.0.0.1:4100/frontcasts/"
        }
        else if (response.status === 400) {
            document.getElementById("error").innerHTML = "Incorrect Login Information"
        }
    }
        ) 
}
// Function to get the value of a cookie by name
function getCookie(name) {
  const value = `; ${document.cookie}`;
  const parts = value.split(`; ${name}=`);
  if (parts.length === 2) return parts.pop().split(';').shift();
}
// Get the JWT cookie value

</script>
</html>
