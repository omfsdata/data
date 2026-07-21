---
layout: default
title: Feedback
nav: feedback
permalink: /feedback/
container: page
---

<p class="eyebrow">Feedback</p>

# Make OMFS Data better
{: .title}

How can I make OMFS Data more useful? Give your anonymous feedback!
{: .byline}

Found an error in the program map, want to see a specific analysis, or have an idea of how to expand this site? Tell me here! Nothing on this form is required except the message itself.
{: .lede}

<!-- ============================================================
     SETUP: replace YOUR_FORM_ID below with your Formspree ID.
     1. Sign up at formspree.io (free tier is fine)
     2. Create a new form -> it gives you an endpoint like
        https://formspree.io/f/xdorwqkv
     3. Paste that whole URL into the action="" attribute below.
     ============================================================ -->
<form class="feedback-form" action="https://formspree.io/f/mrenlzkb" method="POST">

  <label for="topic">What is this about?</label>
  <select id="topic" name="topic">
    <option>Program map</option>
    <option>SDN match analysis</option>
    <option>Data</option>
    <option>Site / usability</option>
    <option>Something else</option>
  </select>

  <label for="message">Your feedback</label>
  <textarea id="message" name="message" rows="20" required
            placeholder="Let me know what you'd like to see on OMFS Data!"></textarea>

  <label for="contact">Contact (optional)</label>
  <input type="text" id="contact" name="contact"
         placeholder="Email">

  <!-- honeypot: hidden from humans, catches spam bots -->
  <input type="text" name="_gotcha" style="display:none" tabindex="-1" autocomplete="off">

  <!-- where the visitor lands after submitting -->
  <input type="hidden" name="_next" value="{{ '/feedback/thanks/' | absolute_url }}">
  <input type="hidden" name="_subject" value="OMFS site feedback">

  <button type="submit">Send feedback</button>
</form>

<p class="form-note">
  The contact field is optional and blank by default — leave it empty and I have no way to identify you.
  
  Submissions are delivered through Formspree, a third-party form service, which may log technical
  request data such as IP addresses on its own servers.
</p>
