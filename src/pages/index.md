## ts block

```ts
import * as CSS from 'csstype';

const style: CSS.Properties = {
  colour: 'white', // Type error on property
  textAlign: 'middle', // Type error on value
};
-    return {
-      placeholderText: "Drag and drop a file here",
-      hashed: "",
-      flight: false,
-    };
+    return {};
```

## diff-ts blocks
### Not getting tokenized properly outside of the diff

```diff-ts
import * as CSS from 'csstype';

const style: CSS.Properties = {
  colour: 'white', // Type error on property
  textAlign: 'middle', // Type error on value
};
-    return {
-      placeholderText: "Drag and drop a file here",
-      hashed: "",
-      flight: false,
-    };
+    return {};
```

```diff-ts
import * as CSS from 'csstype';

const a = "b";
call();

-    return {
-      placeholderText: "Drag and drop a file here",
-      hashed: "",
-      flight: false,
-    };
+    return {};
```

## py block
```py
num1 = 1.5
num2 = 6.3

# Add two numbers
s = num1 + num2

# Display the sum
print('The sum of {0} and {1} is {2}'.format(num1, num2, s))
```

## py-diff block
### Not getting tokenized properly outside of the diff

```diff-py
-num1 = 1.5
+num1 = 2.5
num2 = 6.3

# Add two numbers
s = num1 + num2

# Display the sum
print('The sum of {0} and {1} is {2}'.format(num1, num2, s))
```