## Description

Snippets for creating test scenarios using [TestStack.BDDfy](https://github.com/TestStack/TestStack.BDDfy)

## Shortcuts

### bddfy

Creates an empty test scenario definition, including `Given`, `When` and `Then` step definitions. You'll want to use this each time you create a new test.

```csharp
using TestStack.BDDfy;
```
```csharp
[Fact]
public void ShouldBehaveInACertainWay()
{
    this.Given(_ => _.GivenAnInitialState())
        .When(_ => _.WhenSomethingHappens())
        .Then(_ => _.ThenAConsequenceOfThisIs())
        .BDDfy();
}

private void GivenAnInitialState()
{
    throw new NotImplementedException();
}

private void WhenSomethingHappens()
{
    throw new NotImplementedException();
}

private void ThenAConsequenceOfThisIs()
{
    throw new NotImplementedException();
}
```

### bddfyg

Creates an empty `Given` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void GivenAnInitialState()
{
    throw new NotImplementedException();
}
```

### bddfyw

Creates an empty `When` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void WhenSomethingHappens()
{
    throw new NotImplementedException();
}
```

### bddfyt

Creates an empty `Then` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void ThenAConsequenceOfThisIs()
{
    throw new NotImplementedException();
}
```