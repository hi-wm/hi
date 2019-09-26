---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<h2>Estimated La Croix Consumed <span id="la-croix"></span></h2>

<script>
        let la_croix = document.getElementById("la-croix");
        let one_day = 1000 * 60 * 60 * 24;
        let start = new Date("Sept 03, 2019 08:00:00");
        let today = new Date();
        let day_diff = (Math.round(today.getTime() - start.getTime()) / (one_day)).toFixed(0);
        let minus_weekends = (day_diff.toFixed(0) / 7).toFixed(0);
        let work_days = day_diff - minus_weekends;
        let la_croix_consumed = work_days * 2;
        la_croix.innerHTML = la_croix_consumed;
</script>