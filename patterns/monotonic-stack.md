# Monotonic Stack

## Monotonic Stack

### Monotonic Stack

#### What is it?

Stack is a very simple sturcuture. It is used in problems where we want the elements to follow the first-in-first-out \(FIFO\) pattern.

Monotonic Stack is just a fancy name for a non-deceasing / non-increasing stack. Elements in a simple stack are not ordered. Monotonic Stack uses some special techniques to force the elements in the stack to have an order. Thus, it is particularly useful in problems where we want both the **FIFO** and **Ordered** properties.

The implementation of a monotonic non-deceasing stack looks like this:

```c++
class MonoStack {
  public:
  	int push(int x) {
      // Some magic here to preserve ordering
      stk.push(x);
    }
    
    int pop() {
      stk.pop(); // pop just like we do in an ordinary stack
    }
  private:
  	stack<int> stk; // just a simple stack
}
```

Now, what is the magic to make the elements non-decresing? The answer is simple: Beofore we push an element \(call it `x`\) onto the stack, we pop all elements in the stack that are bigger than `x`. In this way, we make sure that `x` must be the biggest element in the stack.

Below is the implementation for the `push` method:

```c++
int push(int x) {
  // pop all elements that are greater than x
  while(!stk.empty() && stk.top() > x) {
    stk.pop();
  }
  stk.push(x);
}
```

Find some numbers and try it yourself if you are still not sure.

#### When to use it?

Monotonic stack is really easy to understand and to implement. The hardest part is to use it to model and solve problems. Usually, it is not obvious that a problem requires mono stack. However, here are some  signals when you might need a mono stack

- Next greater element
  - This kind of problem asks you to "predict the future" (What is the next greater/smaller element of each element in the array)
- Special stack
  - You have a feeling this is a stack problem. Then you notice that when an element is popped from the stack, it is never used again.
  - You have a feeling this is a stack problem, and the problem also asks for some maxima/minima

#### Practice problems

