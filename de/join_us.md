---
permalink: /de/join_us/
lang: de
title: "Mitmachen"
description: "Offene Stellen, Abschlussarbeiten und Praktika im Labor für Mental Health Mapping an der Friedrich-Schiller-Universität Jena."
---

<p class="highlight">Neugierig, motiviert, freundlich und bereit, anzupacken? Dann freuen wir uns auf Ihre Nachricht.</p>

Wir sind an der Friedrich-Schiller-Universität Jena. Für eine Bewerbung senden Sie [Thomas Wolfers](mailto:dr.thomas.wolfers@gmail.com) bitte Ihren Lebenslauf und eine kurze Darstellung Ihrer Interessen per E-Mail. Das gilt auch, wenn Sie sich mit uns um eine eigene Förderung bewerben möchten (z. B. ein Marie-Curie-Stipendium) oder andere Fragen haben.

## Offene Stellen

Ausschreibungen für Postdoc-, Promotions-, Data-Scientist- und HiWi-Stellen veröffentlichen wir hier.

<!-- The buttons below open the sections in place; edit the text inside each <section>. -->
<h2>Arbeiten bei uns</h2>
<div class="buttons compact toggles">
<a class="button secondary toggle" href="#students">Abschlussarbeiten &amp; Praktika</a>
<a class="button secondary toggle" href="#learn">Wie wir lernen</a>
<a class="button secondary toggle" href="#mentorship">Mentoring</a>
</div>
<section class="toggle-panel" id="students">
<h3>Master- und Bachelorstudierende</h3>
<p>Studierende, die sich für eine Bachelor- oder Masterarbeit oder ein Praktikum interessieren, können sich direkt bewerben oder zunächst an unserem <a href="/de/teaching/#seminar">Seminar mit Auswahlverfahren</a> teilnehmen, um das Labor kennenzulernen.</p>
</section>
<section class="toggle-panel" id="learn">
<h3>Wie wir lernen</h3>
<p>Unser Labor möchte ein Umfeld bieten, in dem Lernen Freude macht, und erkennt zugleich an, dass anspruchsvolle Aufgaben unweigerlich mit innerem Widerstand (z. B. Aufschieben, Selbstzweifel, Angst vor dem Scheitern) und äußerem Widerstand (z. B. kritische Gutachten, Ablehnungen oder wenig positives Feedback) einhergehen. Wir betrachten diese Erfahrungen nicht als Hindernisse, die es zu vermeiden gilt, sondern als festen Bestandteil wissenschaftlicher Entwicklung.</p>
<p>Auch wenn Wissenschaft oft Phasen konzentrierter Einzelarbeit erfordert, schaffen wir, wann immer möglich, Gelegenheiten für gemeinsames Lernen und Reflektieren. Unser Ziel ist es, kompetente, selbstbewusste Forschende auszubilden, die schwierige Probleme angehen und verantwortungsvoll zur Gesellschaft beitragen. Bei uns werden Sie darin bestärkt, sowohl die fachlichen Fähigkeiten als auch die persönlichen Eigenschaften zu entwickeln, die Sie für ehrgeizige Ziele brauchen, ob in der Wissenschaft oder darüber hinaus.</p>
<p>Wir heißen Menschen aller Hintergründe willkommen und schätzen unterschiedliche Perspektiven, Erfahrungen und Wege. Von allen erwarten wir Neugier und die Bereitschaft, hart zu arbeiten; im Gegenzug unterstützen wir alle dabei, im eigenen Tempo und in die eigene Richtung zu wachsen.</p>
</section>
<section class="toggle-panel" id="mentorship">
<h3>Mentoring</h3>
<p>Kompetenzen verändern sich mit der Zeit und je nach Thema. Deshalb ist die Beziehung zwischen Mentor und Mentee dynamisch, nicht festgelegt. Wir versuchen, das Ego dabei außen vor zu lassen.</p>
</section>

<h2>Lernen Sie uns kennen</h2>
<div class="buttons compact">
<a class="button secondary" href="/de/values/">Unsere Werte</a>
<a class="button secondary" href="/de/community/">Community</a>
<a class="button secondary" href="/de/moving_to_jena/">Umzug nach Jena</a>
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
