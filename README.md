# Engaging Networks Custom Validators
Custom validators are great to add additional validation to your pages. They alert the supporter that a field hasn't been input in the correct format. 

You can create new validators by going to **Pages > Alerts & validators > Validators**. When you create a new one, choose the Validator Type of "Custom". The custom code uses a language called "regex". You can learn about regex on sites like https://regexone.com and test your regex code before applying it to your pages at sites like https://regex101.com.

This repository is a fork of Engaging Network's own: https://github.com/EngagingNetworks/custom-validators

### Must contain 100 characters or less
Safe default for Address 2\
Safe default for Region (e.g. State)\
Safe default for Postal Code (e.g. Zip Code)
```regex
^.{0,100}$
```

### Must contain 35 characters or less
Required by Vantiv for Address 1\
Required by Vantiv for City
```regex
^.{0,35}$
```

### Must contain 25 characters or less
Required by Vantiv for First Name\
Required by Vantiv for Last Name
```regex
^.{0,25}$
```

### Phone numbers can only contain the numbers, spaces, pluses, opening parenthesis, closing paranethesis, dashes, and periods
While not in the error message, the value can also be blank
```regex
^$|^[0-9#+()\-. ]{7,25}$
```

### Address can only contain letters, numbers, commas, spaces, dots, slashes, dashes, and apostophes
**This validator is untested but was included on the EN repo and seemed like it could be useful**\
While not in the error message, the value can also be blank
```regex
^$|^[A-Za-z0-9\s\-\\\/.,—'’]+$
```
