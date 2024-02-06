---
layout: home
search_exclude: true
---

# Welcome.
<script>
    function eraseCookie(name) {   
    document.cookie = name+'=; Max-Age=-99999999;';  
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