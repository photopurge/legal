---
title: Retire Roadmap Support
---

# Retire Roadmap Support

**Developer:** Heylon Studio  
**Last updated:** 15 September 2026  
**Contact:** [heylonstudio@gmail.com](mailto:heylonstudio@gmail.com)

Retire Roadmap is a retirement planning app for iPhone, iPad, and Android. Use the form below to ask a question or report a problem. Your message is emailed to **heylonstudio@gmail.com**.

<style>
  .support-form {
    background: #f6f8fa;
    border: 1px solid #d0d7de;
    border-radius: 12px;
    padding: 1.15rem 1.2rem 1.25rem;
    margin: 0 0 1.75rem;
  }
  .support-form label {
    display: block;
    font-weight: 600;
    margin: 0 0 0.35rem;
    font-size: 0.92rem;
  }
  .support-form .field { margin-bottom: 0.85rem; }
  .support-form input,
  .support-form select,
  .support-form textarea {
    width: 100%;
    max-width: 100%;
    box-sizing: border-box;
    padding: 0.6rem 0.7rem;
    border: 1px solid #d0d7de;
    border-radius: 8px;
    font: inherit;
  }
  .support-form textarea { min-height: 140px; resize: vertical; }
  .support-form button {
    appearance: none;
    border: 0;
    border-radius: 8px;
    padding: 0.65rem 1.1rem;
    font: inherit;
    font-weight: 700;
    color: #fff;
    background: #0969da;
    cursor: pointer;
  }
  .support-form button:disabled { opacity: 0.6; cursor: default; }
  .support-form .status { margin: 0 0 0.85rem; font-size: 0.95rem; }
  .support-form .ok { color: #1a7f37; }
  .support-form .err { color: #cf222e; }
  .hp { position: absolute; left: -9999px; height: 0; overflow: hidden; }
</style>

<form class="support-form" id="support-form">
  <strong>Request support</strong>
  <p>We read every message and reply by email as soon as we can.</p>
  <p class="status" id="support-status" role="status"></p>
  <input class="hp" type="text" name="_honey" tabindex="-1" autocomplete="off">
  <div class="field">
    <label for="support-name">Your name</label>
    <input id="support-name" name="name" type="text" required maxlength="120" autocomplete="name">
  </div>
  <div class="field">
    <label for="support-email">Email</label>
    <input id="support-email" name="email" type="email" required maxlength="200" autocomplete="email">
  </div>
  <div class="field">
    <label for="support-app">App</label>
    <select id="support-app" name="app" required>
      <option value="Retire Roadmap" selected>Retire Roadmap</option>
      <option value="Photo Purge">Photo Purge</option>
      <option value="Other">Other / not sure</option>
    </select>
  </div>
  <div class="field">
    <label for="support-message">Description of the issue</label>
    <textarea id="support-message" name="message" required maxlength="4000" placeholder="What you were trying to do, what happened, and your device / app version if you know them."></textarea>
  </div>
  <button type="submit" id="support-submit">Send to heylonstudio@gmail.com</button>
</form>

## What to include

- The device and OS version (for example iPad Air, iPadOS 18)
- The app version from Settings or the App Store listing
- What you were trying to do, and what happened instead
- For purchases: whether you used Monthly, Yearly, or Lifetime, and the Apple ID country if relevant

Please do not email passwords, payment card numbers, or your full portfolio details unless they are needed to reproduce a bug.

## Premium, subscriptions, and restore

Optional Premium unlocks up to eight assets, roadmap exports (PDF / Excel), and an ad-free experience. Payment is handled only by Apple or Google. We never see your card details.

- **Restore a purchase:** open Retire Roadmap, tap the ⋮ menu, then **Restore purchases**. Sign in with the same Apple ID you used to buy.
- **Manage or cancel a subscription:** on your Apple device go to Settings → [your name] → Subscriptions, or use [apps.apple.com/account/subscriptions](https://apps.apple.com/account/subscriptions).
- **Refunds:** request these from Apple via [reportaproblem.apple.com](https://reportaproblem.apple.com/). We cannot issue App Store refunds ourselves.

## Privacy and terms

- [Privacy Policy](/legal/retire-roadmap-privacy.html)
- [Apple Licensed Application End User License Agreement](https://www.apple.com/legal/internet-services/itunes/dev/stdeula/)

## Contact

Heylon Studio  
[heylonstudio@gmail.com](mailto:heylonstudio@gmail.com?subject=Retire%20Roadmap%20support)

<script>
(function () {
  var form = document.getElementById('support-form');
  if (!form) return;
  var statusEl = document.getElementById('support-status');
  var submitBtn = document.getElementById('support-submit');
  var appSelect = document.getElementById('support-app');
  form.addEventListener('submit', function (e) {
    e.preventDefault();
    submitBtn.disabled = true;
    statusEl.className = 'status ok';
    statusEl.textContent = 'Sending…';
    fetch('https://formsubmit.co/ajax/heylonstudio@gmail.com', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json', 'Accept': 'application/json' },
      body: JSON.stringify({
        name: document.getElementById('support-name').value.trim(),
        email: document.getElementById('support-email').value.trim(),
        app: appSelect.value,
        message: document.getElementById('support-message').value.trim(),
        _subject: appSelect.value + ' support request',
        _template: 'table',
        _captcha: 'false'
      })
    }).then(function (res) {
      return res.json().catch(function () { return {}; }).then(function (data) {
        if (!res.ok) throw new Error((data && data.message) || 'Could not send');
      });
    }).then(function () {
      form.reset();
      appSelect.value = 'Retire Roadmap';
      statusEl.className = 'status ok';
      statusEl.textContent = 'Thanks — your message was emailed to heylonstudio@gmail.com. We will reply as soon as we can.';
    }).catch(function () {
      statusEl.className = 'status err';
      statusEl.textContent = 'Could not send from this browser. Email heylonstudio@gmail.com directly and we will help.';
    }).finally(function () {
      submitBtn.disabled = false;
    });
  });
})();
</script>
