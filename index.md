---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<p class="unique-title-name">Estimated La Croix Consumed <span id="la-croix"></span></p>

<script>
        let la_croix = document.getElementById("la-croix");
        let one_day = 1000 * 60 * 60 * 24;
        let start_date = new Date("Sept 03, 2019 08:00:00");
        let today = new Date();
        let day_diff = (Math.round(today.getTime() - start_date.getTime()) / (one_day)).toFixed(0);
        let minus_weekends = (day_diff / 7)*2.toFixed(0);
        let work_days = day_diff - minus_weekends;
        let la_croix_consumed = work_days * 2;
        la_croix.innerHTML = la_croix_consumed;
</script>