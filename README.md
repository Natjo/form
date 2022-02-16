
# Form

![version](https://img.shields.io/github/manifest-json/v/Natjo/formValidate)

Markup and css for accessible forms.  
See [formValidate](https://github.com/Natjo/formValidate) to add native validation. 

## Layout

```html
<form action="myAction" data-nonce="myNonce" novalidate="novalidate" role="form" aria-label="Contact information" data-mandatory="Mandatory field">
    <fieldset>
        <legend>Personal information</legend>

        <div class="field">
        </div>
        ...
        <div class="action">
            <input type="submit">
            <button type="reset">Reset</button>
        </div>
    </fieldset>	
</form>
```
## Text
```html
<div class="field">
    <label for="">Name*</label>
    <input type="text" name="name" required minlength="3" placeholder="3 caracters min" aria-describedby="error-name" data-typemismatch="3 caracters min">
</div>
```

## Email
```html
<div class="field">
    <label for="">Email*</label>
    <input type="email" name="email" required placeholder="Email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$" aria-describedby="error-email" data-patternmismatch="Please type an email">
</div>
```

## Date
```html
<div class="field">
    <label for="">Date*</label>
    <input type="date" name="data" required placeholder="jj/mm/aaaa" aria-describedby="error-date">
</div>
```
## Tel
```html
<div class="field">
    <label for="">Tel*</label>
    <input type="tel" name="tel" required placeholder="(+xx) xxxxxxxx" pattern="^(?:0|\(?\+33\)?\s?|0033\s?)[1-79](?:[\.\-\s]?\d\d){4}$" aria-describedby="error-tel" data-patternmismatch="Tel number must be (+xx) xxxxxxxx">
</div>
```

## Select
```html
<div class="field">
    <label>gender*</label>
    <select title="Select an option" name="gender" required aria-describedby="error-gender">
        <option value="" hidden>Select</option>
        <option value="a">M</option>
        <option value="z">F</option>
    </select>
</div>
```
## Number
```html
<div class="field">
    <label>Age*</label>
	<input type="number" name="age" required min="10" max="100" placeholder="Between 10 and 100" aria-describedby="error-age">
</div>
```
## File
```html
<div class="field">
    <label>Curriculum*</label>
    <input type="file" required name="curriculum"
    aria-describedby="error-curriculum">
</div>
```

## Radio Multi
```html
<div class="field radio" role="group" aria-labelledby="country-label">
    <label id="country-label">Country*</label>
    <ul>
        <li>
            <input id="country-0" type="radio" name="test[]" value="" required aria-describedby="error-country">
            <label for="country-0">France</label>
        </li>
        <li>
            <input id="country-1" type="radio" name="test[]" value="" required aria-describedby="error-country">
            <label for="country-1">England</label>
        </li>
        <li>
            <input id="country-2" type="radio" name="test[]" value="" required aria-describedby="error-country">
            <label for="country-2">Russia</label>
        </li>
    </ul>
</div>
```

## Url
```html
<div class="field">
    <label for="">Website*</label>
    <input type="url" required name="website" placeholder="http://tld.com" aria-describedby="error-website">
</div>
```
## Textarea
```html
<div class="field">
    <label for="">Message*</label>
    <textarea name="msg" required aria-describedby="error-msg"></textarea>
</div>
```

## Checkbox
```html
<div class="field checkbox">
    <input id="newsletter" type="checkbox" name="newsletter" required aria-describedby="error-newsletter">
    <label for="newsletter">Newsletter*</label>
</div>
```

## Checkbox multi
```html
<div class="field checkbox" role="group" aria-labelledby="option-label">
    <label id="option-label">Option</label>
    <ul>
        <li>
            <input id="option-0" type="checkbox" name="option-0" value="" aria-describedby="error-option">
            <label for="option-0">Option 1</label>
        </li>
        <li>
            <input id="option-1" type="checkbox" name="option-1" value="" aria-describedby="error-option">
            <label for="option-1">Option 2</label>
        </li>
        <li>
            <input id="option-2" type="checkbox" name="option-2" value="" aria-describedby="error-option">
            <label for="option-2">Option 3</label>
        </li>
    </ul>
</div>
```

## Password
```html
<div class="field">
    <label for="">Password</label>
    <input type="password" name="password" required placeholder="password" pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{8,}" aria-describedby="error-password">
    <small>
        At least on number, on uppercase letter, and 8 or more characters
    </small>	
</div>
```

## Demo
[See codepen demo](https://codepen.io/natjo/pen/NmMzNd?editors=0011)


