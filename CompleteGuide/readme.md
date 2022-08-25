# css

## rules

- Parent styles are inherited by child elements if not overwritten

- Different Types of Selectors

        h1 {…}
        .some-class {…}
        [disabled] {…}
        #some-id {…}
        * {…
- Inheritance & Specifity

    - Parent styles are generally inherited

    - Multiple rules can apply to one element

    - Specifity resolves “multiple rules” conflicts
    
    - Inheritance defaults can be changed

- Selectors with Combinators

        Adjacent Sibling
            div + p {
                color: red;
            }
        
        General Sibling
            div ~ p {
                color: red;
            }
        
        Child
            div > p {
                color: red;
            }

        Descendant
            div p {
                color: red;
            }

- Cascading Style Sheets & Specificity

    - Inline Styles
    - #ID selectors
    - .class, :pseudo-class and [attribute] selectors
    - <Tag> and ::pseudo-element selectors

- Shorthand Properties

    - Separate properties

            border-width: 2px
            border-style: dashed | solid
            border-color: orange

            margin-top: 5px
            margin-right: 10px
            margin-bottom:5px
            margin-left: 10px

    - Shorthand property

            border: 2px dashed orange
            margin: 5px 10px 5px 10px;
            margin: 5px 10px;