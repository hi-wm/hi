---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<h1>La Croix Consumed<span id="la-croix"></span></h1>

<script>
        let la_croix = document.getElementById("la-croix");
        let start = new Date(09/03/2019);
        let today = new Date(09/30/2019);

        function calculate_la_croix() {
            let la_croix_consumed = (start - today) * 2;
            la_croix.innerHTML = la_croix_consumed;
        }
</script>