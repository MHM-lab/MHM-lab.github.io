---
permalink: /join_us/
title: "Join Us"
description: "Open positions, theses, and internships at the laboratory for Mental Health Mapping, Friedrich Schiller University Jena."
---

<p class="highlight">Curious, driven, kind, and ready to put in the work? We would love to hear from you.</p>

We are based at Friedrich Schiller University Jena. To apply, email [Thomas Wolfers](mailto:dr.thomas.wolfers@gmail.com) your CV and a short statement of your interests. The same applies if you would like to apply for individual funding with us (e.g., a Marie Curie fellowship) or have any other questions.

## Open positions

Open calls for postdoc, PhD, data scientist, and HiWi positions will be posted here.

<!-- The buttons below open the sections in place; edit the text inside each <section>. -->
<h2>Working with us</h2>
<div class="buttons compact toggles">
<a class="button secondary toggle" href="#students">Theses &amp; internships</a>
<a class="button secondary toggle" href="#learn">How we learn</a>
<a class="button secondary toggle" href="#mentorship">Mentorship</a>
</div>
<section class="toggle-panel" id="students">
<h3>Master's and bachelor's students</h3>
<p>Students interested in a bachelor's or master's thesis or an internship are welcome to apply directly, or to first join our <a href="/teaching/#seminar">selective seminar</a> to get to know the lab.</p>
</section>
<section class="toggle-panel" id="learn">
<h3>How we learn</h3>
<p>Our lab aims to provide an environment in which learning is joyful, while recognizing that meaningful challenges inevitably come with both internal resistance (e.g., procrastination, self-doubt, fear of failure) and external resistance (e.g., critical reviews, rejection, or less-than-positive feedback). We treat these experiences not as obstacles to avoid, but as integral parts of scientific growth.</p>
<p>While science often requires periods of focused, solitary work, we actively create opportunities for collaborative learning and shared reflection whenever possible. Our goal is to educate competent, confident researchers who are able to take on difficult problems and contribute responsibly to society. In our lab, you will be encouraged to develop both the technical skills and personal qualities needed to pursue ambitious goals, whether academic or beyond.</p>
<p>We welcome people from all backgrounds and value diverse perspectives, experiences, and paths. We ask everyone for curiosity and a willingness to work hard; in return, we support each person in growing at their own pace and in their own direction.</p>
</section>
<section class="toggle-panel" id="mentorship">
<h3>Mentorship</h3>
<p>Competences change with time and topic, so the relationship between mentor and student is dynamic, not fixed. We aim to keep ego out of it.</p>
</section>

<h2>Get to know us</h2>
<div class="buttons compact">
<a class="button secondary" href="/values/">Our values</a>
<a class="button secondary" href="/community/">Community</a>
<a class="button secondary" href="/moving_to_jena/">Moving to Jena</a>
</div>

<script>
// Buttons open their section in place; clicking again closes it. Without JavaScript the #links still work.
(function () {
  var buttons = document.querySelectorAll('.toggle'), panels = document.querySelectorAll('.toggle-panel');
  function show(id) {
    panels.forEach(function (p) { p.classList.toggle('open', p.id === id); });
    buttons.forEach(function (b) { b.setAttribute('aria-expanded', b.getAttribute('href') === '#' + id ? 'true' : 'false'); });
  }
  buttons.forEach(function (b) {
    b.setAttribute('aria-expanded', 'false');
    b.addEventListener('click', function (e) {
      e.preventDefault();
      var id = b.getAttribute('href').slice(1), isOpen = b.getAttribute('aria-expanded') === 'true';
      show(isOpen ? '' : id);
      history.replaceState(null, '', isOpen ? location.pathname : '#' + id);
    });
  });
  var h = location.hash.slice(1); if (h && document.getElementById(h) && document.getElementById(h).classList.contains('toggle-panel')) show(h);
})();
</script>
