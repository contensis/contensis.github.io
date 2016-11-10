# Query Operators

## Logical Operators

{% method -%}

### And

This would return any document where first is 1 AND second is 2.
The **And** operator is the default logical operator and is not required to be specified explicitly.

{% sample lang="json" -%}
```json
{
    "where": [{
        "and": [{
            "field": "first",
            "equalTo": 1
        }, {
            "field": "second",
            "equalTo": 2
        }]
    }]
}
```
Is equivalent to:
```json
{
    "where": [{
        "field": "first",
        "equalTo": 1
    }, {
        "field": "second",
        "equalTo": 2
    }]
}
```

{% sample lang="cs" -%}
```cs
var query = new Query(
    Op.And(
        Op.EqualTo("first", 1),
        Op.EqualTo("second", 2)
    )
);
```
Is equivalent to:

```cs
var query = new Query(
    Op.EqualTo("first", 1),
    Op.EqualTo("second", 2)
);
```

{% endmethod %}

---

{% method -%}

### Or

The example would return any document where first is 1 OR second is 2.

{% sample lang="json" -%}
```json
{
    "where": [{
        "or": [{
            "field": "first",
            "equalTo": 1
        }, {
            "field": "second",
            "equalTo": 2
        }]
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.Or(
        Op.EqualTo("first", 1),
        Op.EqualTo("second", 2)
    )
);
```

{% endmethod %}

---
{% method -%}

### Not

The not expects an inner operator so in the example any document where first is not equal to 7 would be returned.

{% sample lang="json" -%}
```json
{
    "where": [{
        "not": {
            "field": "first",
            "equalTo": 7
        }
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.Not(Op.EqualTo("first", 7))
);
```

{% endmethod %}

---

## Relational & Equality Operators

{% method -%}
### Between

In this example if our field is between 18 and 45 (inclusive) it would match.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "age",
        "between": [18, 45]
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.Between("age", 18, 45)
);
```

{% endmethod %}

---
{% method -%}
### Contains

This would match on a field called description containing the phrase 'batman'

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "description",
        "contains": "espresso"
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.Contains("description", "batman")
);
```

{% endmethod %}

---
{% method -%}
### EndsWith

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "wordField",
        "endsWith": "ing"
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.EndsWith("wordField", "ing")
);
```

{% endmethod %}

---
{% method -%}
### EndsWith

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "blends",
        "equalTo": 5
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.EqualTo("blends", 5)
);
```

{% endmethod %}

---
{% method -%}
### Exists

In the example any document that has a field called fieldName would be returned.
You can use a value of false if you want documents that do not contain a given field.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "fieldName",
        "exists": true
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.Exists("fieldName", true)
);
```

{% endmethod %}

---
{% method -%}
### GreaterThan

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "greaterThan": 7
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
  Op.GreaterThan("first", 7)
);
```

{% endmethod %}

---
{% method -%}
### GreaterThanOrEqualTo

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "greaterThanOrEqualTo": 7
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.GreaterThanOrEqualTo("first", 7)
);
```

{% endmethod %}

---
{% method -%}
### In

In the example any document that where the field *first* is equal to 1,7 or 11 would be returned.
The values should be of the same type, in this case *integer*

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "in": [1, 7, 11]
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.In("first", 1, 7, 11)
);
```

{% endmethod %}

---
{% method -%}
### LessThan

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "lessThan": 7
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.LessThan("first", 7)
);
```

{% endmethod %}

---
{% method -%}
### LessThanOrEqualTo

TODO: example description

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "lessThanOrEqualTo": 7
    }]
}
```

{% sample lang="cs" -%}

```cs
var query = new Query(
    Op.LessThanOrEqualTo("first", 7)
);
```

{% endmethod %}

---
{% method -%}
### StartsWith

In the example if our field contains a word starting with ‘war’ it would match.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "name",
        "startsWith": "war"
    }]
}
```

{% sample lang="cs" -%}

```cs

```

{% endmethod %}

---