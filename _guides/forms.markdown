---
breadcrumbs: true
title: Form Elements
layout: article
published: true
---

<form>
  <p class="message">Generic message</p>
  <p class="message message--error">Error message</p>
  <p class="message message--success">Success message</p>

  <label for="field-text" class="required">Text field <span>*</span></label>
  <input id="field-text" type="text" placeholder="Placeholder text" />

  <label for="field-number">Number field</label>
  <input id="field-number" type="number" placeholder="123" />

  <label for="field-date">Date field</label>
  <input id="field-date" type="date" />

  <label>Textarea</label>
  <textarea></textarea>

  <label>
    <input type="checkbox">
    Checkbox
  </label>

  <br />

  <label>
    <input type="radio">
    Radio
  </label>

  <br />

  <label>Select</label>
  <select>
    <option>Option</option>
    <option>Another Option</option>
  </select>
</form>
