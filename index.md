---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<h1>La Croix Consumed<span id="la-croix"></span></h1>

<script>
        let la_croix = document.getElementById("la-croix");
        let one_day = 1000 * 60 * 60 * 24;
        let start = new Date("Sept 03, 2019 08:00:00");
        let today = new Date();
        let la_croix_pre = Math.round(today.getTime() - start.getTime()) / (one_day);
        let la_croix_consumed = la_croix_pre.toFixed(0);
        la_croix.innerHTML = la_croix_consumed;
</script>