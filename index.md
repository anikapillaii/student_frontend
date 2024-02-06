---
layout: home
search_exclude: true
---

<script>
    window.addEventListener("load", (event) => {
        console.log("hi")
        isCookie = document.cookie.match(/^(.*;)?\s*jwt\s*=\s*[^;]+(.*)?$/)
        if (isCookie) {
            console.log("true")
        }
        else {
            console.log("nuh uh")
        }
    })
</script>



# Posts
