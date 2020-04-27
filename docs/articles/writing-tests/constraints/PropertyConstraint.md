`PropertyConstraint` tests for the existence of a named property on an object and then
applies a constraint test to the property value.

#### Constructor

```C#
PropertyConstraint(string name, IConstraint baseConstraint)
```

#### Syntax

```C#
Has.Property(string name)... // followed by further constraint syntax
```

#### Examples of Use

```C#
Assert.That(someObject, Has.Property("Version").EqualTo("2.0"));
Assert.That(collection, Has.Property("Count").GreaterThan(10));
Assert.That(collection, Has.Count.GreaterThan(10);
```

**Note:** As shown in the example, certain common properties are known to NUnit and 
may be tested using a shorter form. The following properties are supported:

```C#
Has.Length...
Has.Count...
Has.Message...
Has.InnerException...
```

#### See also...
 * [[PropertyExistsConstraint]]