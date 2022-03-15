# DAY 1
**Focus** ==[Keeping Components Pure](https://beta.reactjs.org/learn/keeping-components-pure)

Pure components are components do satisfy to rules.

1. it does not modify objects or variables that exist before it was called.
2. It gives the same output for the sample input.

A pure function simple does calculations.
Just like mathematical functions

### Example
`y = 2x;`

Key Points:

- ***Side effects*** or ***mutation*** are best handled with event handlers. or as a last resort useEffect hook.

- ***States*** should be updated using the setState method.

- ***Props*** and ***Inputs*** should not be modified directly.

- Local mutations are components little secret. They are acceptable, and don't make functions impure.

- In ***strict mode*** component functions are called twice


