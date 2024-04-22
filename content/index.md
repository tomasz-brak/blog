---
title: Error
---
It looks like there was some error in the page, we are working on getting you moving again

[English page](/en)

[Polish page](/pl)

<p>Automatic redirect in <span id="countdown">5</span> seconds...</p>

<script>
    const countdownElement = document.getElementById('countdown');
let seconds = 5; // Change this to your desired countdown time

const interval = setInterval(() => {
  countdownElement.textContent = seconds;
  seconds--;
  if (seconds <= 0) {
    clearInterval(interval);
    window.location.replace("/en"); 
  }
}, 1000);
</script>