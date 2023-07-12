@types/react 18.2.* are incompatible with 18.0.*

To reproduce:

```sh
cd library && yarn && yarn build && cd ../application && yarn && yarn build
```

Application is on @types/react 18.0.26 
Library is on @types/react 18.2.14

Typechecking library outputs in application fails with:

```
library-dist/index.d.ts:3:21 - error TS2694: Namespace 'React' has no exported member 'JSX'.

3     render(): React.JSX.Element;
                      ~~~


Found 1 error in library-dist/index.d.ts:3
```