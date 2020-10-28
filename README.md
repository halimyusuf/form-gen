### To use the FormGenerator component, the _name and label_ property is important in the object, the name property is used to manage the state of each input field, hence name of each field must be unique to achieve the desired result, FormGenerator _supports all input types_ that doesn't require an action(button, reset and submit types), input types also supports all attributes which applies to it. ###

 ----------

#### FormGenerator also supports form validation(property name --> validations), it accepts an array of functions which either ___returns true or form error text___ ####.

## Netlify link <https://wizardly-varahamihira-54486e.netlify.app>

#### An example of FormGenerator object

```
[
  {
    label: 'What is the name of the officer in question?',
    type: 'text',
    name: 'office name',
    validations: [
      (_) => !!_ || 'Officer name is required',
      (_) => _.length >= 3 || 'Minimum length 3 char is allowed',
    ],
    placeholder: 'Officer name'
  },
  {
    label: 'When was the date of the incident?',
    type: 'date',
    name: 'incident date',
  },
  {
    label: 'How much is the bribe that was paid? (optional)',
    type: 'number',
    name: 'bribe paid',
  },
  {
    label: 'Are you a vegetarian',
    type: 'checkbox',
    name: 'isVegetarian',
  },
  {
    label: 'Gender',
    type: 'select',
    name: 'gender',
    options: ['', 'Male', 'Female', 'Prefer not to say'],
    validations: [(_) => !!_ || 'Gender is required'],
  },
]

```

NB: App hosted on netlify needs to be refreshed if apply changes is clicked and javascript code is invalid.
