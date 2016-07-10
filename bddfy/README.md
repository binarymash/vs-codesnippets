## Description

Snippets for creating test scenarios using the Fluent API of [TestStack.BDDfy](https://github.com/TestStack/TestStack.BDDfy)

## Installation

See https://github.com/binarymash/vs-codesnippets/tree/master/README.md

## Shortcuts

### bddfyfull

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

### bddfy

Creates an empty test scenario definition without any step definitions. You'll want to use this if your scenario is mostly reusing existing step definitions.

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
```

### given

Creates an empty `Given` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void GivenAnInitialState()
{
    throw new NotImplementedException();
}
```

### when

Creates an empty `When` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void WhenSomethingHappens()
{
    throw new NotImplementedException();
}
```

### then

Creates an empty `Then` implementation for a test scenario definition. You might want to use this when adding extra step definitions to your test scenario.

```csharp
private void ThenAConsequenceOfThisIs()
{
    throw new NotImplementedException();
}
```