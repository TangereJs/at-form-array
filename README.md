# at-form-array

#### Null value handling
When value is set as attribute and value is set to `null` (keyword `null`)
 * `null` keyword is converted to `"null" string` value
 * `_valueChanged` function detects string and assumes its a json string
 * `_valueChanged` function tries to `JSON.parse` it
 * `"null" string` value is converted to `null` keyword value

When  value is set as attribute and value is set to `"null" string` value the same happens as described above.

When value is set as property in code and value is set to `null` (keyword `null`)
 * `_valueChanged` function detects that value is `null` and value remains `null`

When value is set as property in code and value is set to `"null" string` value
 * `_valueChanged` function detects string and assumes its a json string
 * `_valueChanged` function tries to `JSON.parse` it
 * `"null" string` value is converted to `null` keyword value

When user tries to add a new entry to the `at-form-array.value` and value is `null`, value is first set to empty array `[]` and then a new item is added
