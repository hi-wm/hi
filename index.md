---
title: 
---
[Resources](./resources.md)  
[Worknotes](./worknotes.md)

<footer>
<p>William has consumed <span id="la-croix"></span> cans of delicious, bubbly, essenced water (La Croix) since his start date at Horizontal.</p>
<p class="lighten-up"><em> * cans of La Croix consumed accurate by ±50%</em></p>
</footer>

<script>
        let la_croix = document.getElementById("la-croix");
        let one_day = 1000 * 60 * 60 * 24;
        let start_date = new Date("Sept 03, 2019 08:00:00");
        let today = new Date();
        let day_diff = (Math.round(today.getTime() - start_date.getTime()) / (one_day)).toFixed(0);
        let minus_weekends = ((day_diff / 7).toFixed(0))*2;
        let work_days = day_diff - minus_weekends;
        let la_croix_consumed = (work_days + 1) * 2;
        la_croix.innerHTML = la_croix_consumed;
</script>