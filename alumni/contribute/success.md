---
layout: single
title: Contribution succeeded
type: page
parent_id: '0'
published: true
password: ''
status: publish
categories: []
tags: []
---

<script src="https://js.stripe.com/v3/"></script>
<h1>Your donation succeeded</h1>
<h4>Checkout Session ID: <span id="session"></span></h4>
<script>
      var urlParams = new URLSearchParams(window.location.search);

      if (urlParams.has("session_id")) {
        document.getElementById("session").textContent = urlParams.get(
          "session_id"
        );
      }
</script>

