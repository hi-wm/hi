---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<h1>La Croix Consumed<span id="la-croix"></span></h1>

<script>
        let la_croix = document.getElementById("la-croix");
        let la_croix_consumed = 0;
        let today = new Date();
        la_croix.innerHTML = la_croix_consumed;

        function calculate_la_croix() {
            let tomorrow = new Date();
            tomorrow.setTime(today.getTime() + la_croix_consumed * 86400000);
            la_croix.innerHTML = tomorrow;
        }
</script>