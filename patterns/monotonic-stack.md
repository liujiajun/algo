# Monotonic Stack

## Monotonic Stack

### Monotonic Stack

#### What is it?

Stack is a very simple sturcuture. It is used in problems where we want the elements to follow the first-in-first-out \(FIFO\) pattern.

Monotonic Stack is just a fancy name for a non-deceasing / non-increasing stack. Elements in a simple stack are not ordered. Monotonic Stack uses some special techniques to force the elements in the stack to have an order. Thus, it is particularly useful in problems where we want both the **FIFO** and **Ordered** properties.

Below is the API for a monotonic non-deceasing stack:

```text

```

Now, how do we make the elements non-decresing? The answer is simple: Beofore we push an element \(call it `x`\) onto the stack, we check the current top element in the stack. If it is bigger than `x`, we pop it. We reapeat this until the current top element in the stack is smaller than or equal to `x`, and then we push `x` onto the stack. In this way, we make sure that the stack is non-deceasing all the time.

Below is the complete implementation for a monotonic non-deceasing stack:

```text

```

Find some numbers and try it yourself if you are still not sure.

#### When to use it?

#### Practice problems

