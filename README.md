# Lab 03 — HTML Form

COS10026 Web Technology Project · Week 03 lab exercise.

An appointment booking form for the CWA Help Desk.

## Files

| File | Description |
|------|-------------|
| `helpdesk.html` | The CWA Help Desk appointment form |
| `images/logo.png` | Swinburne logo from the lab files (199 x 100 PNG) |
| `README.md` | This document |

## Steps Followed

1. **File structure** — document declaration, `<html>` with `<head>` and `<body>`, meta tags for
   charset, description, keywords and author, and the title `CWA Help Desk Appointment`.
2. **Form content** — the logo linked to `http://www.swin.edu.au`, a heading, two paragraphs and
   the form, using `example_form.html` as the exemplar.
3. **Input checking** — `required` and `pattern` attributes on the inputs.
4. **Revalidation** — the page was checked again with the W3C validator.

## Form Elements

- `<form method="post" action="...">` holding all the controls
- `<fieldset>` and `<legend>` grouping Student details, Your unit, Issue and Preferred Date / Time
- `<label for="...">` linked to the `id` of each control, and a `name` on every control
- `<input type="radio">` for the unit, all sharing `name="unit"`
- `<select>` for the tutor, with an empty first option `<option value="">Please Select</option>`
- `<input type="checkbox">` for the issue, sharing the array name `issue[]`, with HTML ticked by
  `checked="checked"`
- `<textarea>` for the description, with a `placeholder`
- `<input type="submit">` (Book) and `<input type="reset">` (Reset form)

## Input Checking

| Field | Rule | Attributes |
|-------|------|------------|
| Student ID | required, 7 to 10 digits | `pattern="\d{7,10}"`, `maxlength="10"` |
| Given Name, Family Name | required, letters only, at most 15 characters | `pattern="[A-Za-z]+"`, `maxlength="15"` |
| Your unit | one unit must be chosen | `required="required"` on the first radio button |
| Your Tutor | a tutor must be chosen | `required="required"` with an empty first option |
| Date | required, matches `dd/mm/yyyy` | `pattern="\d{2}/\d{2}/\d{4}"` |
| Time | required, matches `00:00`, hours 00 to 23 | `pattern="([01]?[0-9]|2[0-3]):[0-5][0-9]"` |

Date and Time were first built with `<input type="date">` and `<input type="time">`. Firefox and
Chrome show these controls differently (each browser draws its own date and time picker), so they
were changed to `type="text"` with `placeholder` and `pattern` attributes, as the lab asks.

## Validation

`helpdesk.html` was checked with the
[W3C Markup Validation Service](https://validator.w3.org/#validate_by_input)
after each step: no errors and no warnings.

## How to View

Clone the repository:

```bash
git clone https://github.com/dangminh232006/lab03.git
```

Then open `helpdesk.html` in Firefox.

## Author

Bui Dang Minh (105716425) — Swinburne University
