# Query operators

## Logical Operators

{% method -%}

### And

This would return any document where first is 1 AND second is 2.
The *And* operator is the default logical operator and is not required to be specified explicitly.

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

{% endmethod %}

---

{% method -%}

### Or

The example would return any document where *first* is *1* OR *second* is *2*.

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

{% endmethod %}

---
{% method -%}

### Not

The not expects an inner operator so in the example any document where *first* is NOT equal to *7* would be returned.

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

{% endmethod %}

---

## Relational & equality operators

{% method -%}
### Between

In this example, if our field is between *18* and *45* (inclusive) it would match.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "age",
        "between": [18, 45]
    }]
}
```

{% endmethod %}

---
{% method -%}
### Contains

This would match on a field called *description* containing the phrase 'batman'.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "description",
        "contains": "espresso"
    }]
}
```

{% endmethod %}

---
{% method -%}
### EndsWith

This would find any item that has a field called *wordField* with a value ending with 'ing'.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "wordField",
        "endsWith": "ing"
    }]
}
```


{% endmethod %}

---
{% method -%}
### EqualTo

This would find any item that has a field called *blends* with a value exactly matching '5'. For string fields, the comparison is case-insensitive.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "blends",
        "equalTo": 5
    }]
}
```

{% endmethod %}

---
{% method -%}
### Exists

In the example any document that has a field called *fieldName* would be returned.
You can use a value of *false* if you want documents that do not contain a given field.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "fieldName",
        "exists": true
    }]
}
```
{% endmethod %}

---
{% method -%}
### GreaterThan

In the example any item that has a field called *first* and a value that is greater than 7 would be returned.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "greaterThan": 7
    }]
}
```
{% endmethod %}

---
{% method -%}
### GreaterThanOrEqualTo

In the example any item that has a field called *first* and a value that is greater than or equal to 7 would be returned.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "greaterThanOrEqualTo": 7
    }]
}
```
{% endmethod %}

---
{% method -%}
### In

In the example any document that where the field *first* is equal to 1,7 or 11 would be returned.
The values should be of the same type, in this case *integer*.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "in": [1, 7, 11]
    }]
}
```
{% endmethod %}

---
{% method -%}
### LessThan

In the example any item that has a field called *first* and a value that is less than to 7 would be returned.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "lessThan": 7
    }]
}
```
{% endmethod %}

---
{% method -%}
### LessThanOrEqualTo

In the example any item that has a field called *first* and a value that is less than or equal to 7 would be returned.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "first",
        "lessThanOrEqualTo": 7
    }]
}
```
{% endmethod %}

---
{% method -%}
### StartsWith

In the example if the *name* field contains a value starting with ‘war’ it would match.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "name",
        "startsWith": "war"
    }]
}
```
{% endmethod %}

---

{% method -%}
### FreeText

In the example the field 'synopsis' is searched upon for any words that match 'gotham' or 'dark' or 'knight'.

{% sample lang="json" -%}
```json
{
    "where": [{
        "field": "synopsis",
        "freeText": "gotham dark knight"
    }]
}
```
{% endmethod %}

---
