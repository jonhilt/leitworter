# Test seams

**What it is:**

A place you can change behaviour in tests without editing the production path.

**When / why:**

A place where you can alter a program's behaviour without changing the code in that place.

In other words, a point where you can substitute a different implementation in, often useful for testing without hitting real implementations.

You might use interfaces and have a test pass in a stub/mock.

```csharp
public interface ICustomerRepository
{
    Customer Load(int customerId);
}

public interface ITaxService
{
    decimal GetRate(Address address);
}

public class OrderService
{
    private readonly ITaxService taxService;

    public OrderService(ITaxService taxService)
    {
        this.taxService = taxService;
    }

    public decimal CalculateTotal(int total, Address customerAddress)
    {       
        var tax = taxService.GetRate(customerAddress);
        return total * (1 + tax);
    }
}
```

This doesn't just mean "use interfaces", there are other ways to open up a seam for behaviour to be changed without rewriting the code inside.

```csharp
public decimal GetPrice(Product product, Func<Product, decimal> discount)
{
    return product.Price - discount(product);
}
```

Use test seams when you need tests around code that hits a clock, filesystem, HTTP, or database. Ask for a seam so tests can substitute a dependency at one join, and production stays on the real path.

**Exact prompt (leading word):**

> test seams

Use the phrase when talking about where to inject tests or substitutes. Skip the textbook digression.

**Why denser than a tip:**

Names Feathers' idea: a place you can alter behaviour in tests without editing production paths.

**Source:**

- Concept: Michael Feathers, *Working Effectively with Legacy Code*
- As a Leitwort for agents: Matt Pocock, 16 Jun 2026 — https://x.com/mattpocockuk/status/2066922013000671731

**Optional gloss (Matt):**

> For engineering, leading words like "tracer bullets", "deep modules", "test seams", "clean code" are outrageously effective for leading the agent to produce better code.

**Related:**

- [Tracer bullets](tracer-bullets.md)
- [Deep modules](deep-modules.md)
