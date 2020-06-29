LINQ is implemented in two different ways:
 - Extension methods (they are actually called operators).
 - Query expression syntax: SQL-like syntax directly embedded into C#.
 
 LINQ operators are higher-order functions:
 - Functions taking functions e.g: Func<T, bool>
 
 LINQ operators present a fluent interface
 - Calls can be chained Where().Select().ToList()

IEnumerable<T>

All collection types (List,Dictionary, array, etc.) implement this interface.
LINQ operators which are implemented as extension methods on IEnumerable<T>, taking Func<> arguments are named
LINQ to objects and used for in-memory objects.
    
LINQ operators which are implemented as extension methods on IQueryable<T>, taking Expression<> arguments are named
LINQ to entities and used for database and remote connections.

Enumerable: IEnumerable - class which contains LINQ extension method definitions.
