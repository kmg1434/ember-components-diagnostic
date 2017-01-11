# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    [route] -> [temlate] -> [component1]
                      '---> [component2]

    A list of lists where each list of lists is also a list could be modeled by
    a list of lists, where each list is a component.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    - directory inside the app/application/components
    - template.hbs inside directory
    - component.js file inside directory
    - test file in tests/integration/components/example-list/component-test.js

    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{my-contact contact=model}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each my-phone as |phone|}}
      {{my-phone phone=phone}}
    {{/each}}
    ```
