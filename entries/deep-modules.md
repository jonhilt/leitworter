# Deep modules

**What it is:**

A lot of behaviour behind a small interface. Callers stay simple because the module hides the work.

**When / why:**

When a module/part of your system needs to handle substantial functionality.  Its implementation may be complicated but the rest of the system shouldn't need to deal with the complexity.

The desired state is a relatively thin/simple interface, that the rest of the system can talk to, with the complexity hidden in the module itself (not exposed to outside callers).

The opposite is a shallow module, where it has a large interface but relatively small or trivial implementation.

The goal is to pull complexity downward. The module can absorb that complexity so the rest of the system doesn't have to deal with it.

For example, say you need to save an order.

A shallow design might expose all the steps:

``` csharp
await connection.OpenAsync();
await transaction.BeginAsync();

var orderId = await orderRepository.InsertOrderAsync(order);
await orderRepository.InsertLinesAsync(orderId, order.Lines);
await inventory.ReserveAsync(order.Lines);
await payment.AuthorizeAsync(order.Payment);
await transaction.CommitAsync();
```

But now the caller needs to understand database connections, transactions, how order lines are inserted, inventory reservation...

A deeper module might be called like this:

``` csharp
var result = await checkout.PlaceOrderAsync(command);
```

Inside, the implementation carries all the complexity, and the caller has a much smaller conceptual burden (know how to call the PlaceOrder method and handle any results).

**Exact prompt (leading word):**

> deep modules

Use the phrase in design and review. Do not expand it into a design essay unless asked.

**Why denser than a tip:**

Names Ousterhout's idea: a lot of behaviour behind a small interface.

**Source:**

- Concept: John Ousterhout, *A Philosophy of Software Design*
- As a Leitwort for agents: Matt Pocock, 16 Jun 2026 — https://x.com/mattpocockuk/status/2066922013000671731

**Optional gloss (Matt):**

> For engineering, leading words like "tracer bullets", "deep modules", "test seams", "clean code" are outrageously effective for leading the agent to produce better code.

**Related:**

- [Tracer bullets](tracer-bullets.md)
- [Test seams](test-seams.md)
