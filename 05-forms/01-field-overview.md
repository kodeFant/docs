# Field Overview

You need a checkbox, a date and a textarea? No problem, Typemill provides it all...

[TOC]

## Elements of a Field

Typically a field definition consists of:

* The **field-type** (text, select, checkbox and more).
* A **label**.
* A **description** (displayed below the field).
* A **help-text** (displayed as question mark that displays an info box on hover).
* **Attributes** (like "required", "placeholder", and more).

## Field Types

Right now, TYPEMILL provides the following field types:

````
type: checkbox
type: checkboxlist
type: color
type: date
type: email
type: hidden
type: number
type: password
type: radio
type: select
type: text
type: textarea
type: tel
type: url
type: fieldset
type: paragraph
````

## Field Attributes

TYPEMILL supports these boolean attributes (with value: true):

````
auto: true
checked: true
disabled: true
formnovalidate: true
multiple: true
readonly: true
required: true
````

TYPEMILL supports the following attributes with values:

````
id: 'myId'
class: 'myClass'
pattern: '[0-9]{4}'
placeholder: 'my placeholder-text here'
maxlength: 60
min: 1
max: 10
size: 5
rows: 5
cols: 5 
````

The `pattern` attribute accepts every valid regex for input validation in the frontend. Please note, that there is also a backend validation that might conflict with your frontend validation pattern. So please double check your validation pattern, and test the input intensively. You should, of course, only use attributes like `required`, `placeholder`, `rows`, or `cols` if these attributes are valid in HTML for the field type.

## Examples

Just copy & paste the required field-types from the examples below to create your desired form. You can combine the attributes in all ways that are valid for HTML forms.

### checkbox

Creates a simple checkbox. Note that the HTML label (which appears on the right side of the checkbox) is created with `checkboxlabel`. The `label` is added above the checkbox so that it is looks like the label of the other field-types.

````
forms:
  fields:
   
    mycheckbox:
      type: checkbox
      label: Label (Headline) above the checkbox
      checkboxlabel: HTML-label on the right side of the checkbox
      checked: true
````

### checkboxlist

If you want a collection of several checkboxes grouped together, then you can use a checkboxlist like this:

````
forms:
  fields:
   
    mylistofcheckboxes:
      type: checkboxlist
      label: Please check all checkboxes
      options:
        checkbox1: Label for checkbox 1
        checkbox2: Label for checkbox 2
        checkbox3: Label for checkbox 3
````

### color

Adds a color picker. 

**Limitation:** The configuration fields for themes and plugins use a customized color-picker. Public forms and meta-tabs use the standard HTML5 color-picker.

````
forms:
  fields:
   
    mycolors:
      type: color
      label: Background-Color
      placeholder: Add hex color value like #ffffff
      help: If you do not know the hex-values, then google it.
      description: This will change the background color of your page.
      required: true
````

### date

The standard HTML5 datepicker will be used.

````
forms:
  fields:
   
    mydate:
      type: date
      label: Please choose a day.
````

### email

Will only accept valid e-mail-formats.

````
forms:
  fields:
   
    myemail:
      type: email
      label: Add your e-mail
      placeholder: your@email-adress.io
````

### fieldset

If you have a lot of fields, then you can group them together with a fieldset. You can use any fields inside a fieldset of course. 

**Limitation**: This does not work for meta-tabs right now.

````
forms:
  fields:
   
    myfieldset:
      type: fieldset
      legend: Appears as legend or headline for the field-group
      fields: 
        mytextfield:
          type: text
          label: My Label
        mycheckbox:
          type: checkbox
          label: Please check
          checkboxlabel: Do you want to check me?
````

### hidden

If you really need a hidden field, don't forget to add a value. 

**Limitation:** The field does not work for meta-tabs right now.
 
````
forms:
  fields:
   
    myhiddenfield:
      type: hidden
      value: Do not forget to add a value
````

### number

Accepts only numbers.

````
forms:
  fields:
   
    mynumber:
      type: number
      label: Add a number
      min: 1
      max: 10
````

### password

If you want to hide information on user input.

````
forms:
  fields:
   
    mypassword:
      type: password
      label: Enter your password
````

### radio

Radio buttons are created with options like this:

````
forms:
  fields:
   
    myradiobuttons:
      type: radio
      label: Please Choose
      options:
        option1: Yes
        option2: No
        option3: I do not know
````

### select

Select fields are created with options like this:

````
forms:
  fields:
   
    theme:
      type: select
      label: Select A Theme
      options:
        edgeless: Edgeless Theme
        block: Block Theme
        classic: Classic Theme
````

### text

Generates a standard text-input field.

````
forms:
  fields:
   
    mytextfield:
      type: text
      label: Please add a title
      placeholder: My Title
      maxlength: 50
      pattern: '[a-zA-Z0-9 ]'
      class: 'standard-title'
      id: 'mytitle'
````

### textarea

A textarea does not accept any HTML tags or code, but it always accepts Markdown. If you render textarea input as Markdown, you should notify the user about this (use the label or the description for this).

````
forms:
  fields:
   
    myfieldname:
      type: textarea
      label: Add a message
      rows: 5
      description: You can use markdown here.
      help: Check the website XYZ for a markdown reference
````

### tel

Gernerates a HTML5 input field for telephone numbers.

````
forms:
  fields:
   
    mytelfield:
      type: tel
      label: Add your phone number
````

### url

This field only accepts a full URL with a protocol like http, https, ftp, or similar.

````
forms:
  fields:
   
    myurlfield:
      type: url
      label: Please add a valid url
      placeholder: https://typemill.net
````

### paragraph

A paragraph is a pure text. A paragraph field accepts Markdown, but does not provide any other options than a value.

**Limitation:** This does not work for meta-tabs right now.

````
forms:
  fields:
   
    legalnotice:
      type: paragraph
      value: This is my text that should be displayed in the form.
````

Paragraphs can be useful for [public forms](/for-developers/documentation/public-forms), e.g. if you want to add a legal notice or a longer explanation. It is also possible to use the user input of another plugin-field for the paragraph, so the user can edit, for another example, the legal notice of a contact form.

