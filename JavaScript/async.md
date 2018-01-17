## Asynchronous Javascript - Notes from Kyle Simpson talk on Lynda

### Parallel vs. Async

Parallel - like waiting in line for a rollercoaster. Once you get to the front, there are 30 seats and 30 people get on.

Non-Parallel - once you get to the front only you are allowed to get on. Very inefficient.

Concurrency - two higher level tasks happening in the same timeframe. 

Callback hell doesn't necessarily have to do with deep nesting. 

Problems with callbacks:
**Inversion of Control** - when we use callbacks, we are trusting that the data won't come back too early/late/many times/few times, no lost context, no swallowed errors. There is no solution to this with callbacks.

**Not *reason*able** - they can't reason with actions happening.

