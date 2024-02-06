---
layout: home
search_exclude: true
---

<script>
let options = {
    method: 'GET',
    headers: {
        'Content-Type':
            'application/json;charset=utf-8'
    }
}
fetch("http://127.0.0.1:8086/api/users/", options)
.then(response => {
    console.log(response.json())
})
</script>



# Posts
