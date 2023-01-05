# Requirements

## Types

* [Numbers](requirements.md#numbers)
* [Strings](requirements.md#strings)

## Numbers

Compare two numbers using math operations. The requirement uses [Doubles](https://docs.oracle.com/javase/9/docs/api/java/lang/Double.html), meaning decimals are supported.

### Format <a href="#numbers-format" id="numbers-format"></a>

```yaml
type: operation # See below
left: number    # or placeholder that returns a number
right: number   # or placeholder that returns a number
```

### Equal (==) <a href="#numbers-equal" id="numbers-equal"></a>

Check if the numbers are equal

```yaml
type: '=='
left: 10
right: 15
# Result: false, 10 and 15 are not equal
```

### Greater (>) <a href="#numbers-greater" id="numbers-greater"></a>

Check if `left` is greater than `right`

```yaml
type: '>'
left: 10
right: 15
# Result: false, 10 is not greater than 15
```

### Greater or equal (>=) <a href="#numbers-great_or_equal" id="numbers-great_or_equal"></a>

Check if `left` is greater or equal to `right`

```yaml
type: '>='
left: 20
right: 15
# Result: true, 20 is greater or equal to 15
```

### Smaller (<) <a href="#numbers-smaller" id="numbers-smaller"></a>

Check if `left` is smaller than `right`

```yaml
type: '<'
left: 10
right: 15
# Result: true, 10 is smaller than 15
```

### Smaller or equal (<=) <a href="#numbers-smaller_or_equal" id="numbers-smaller_or_equal"></a>

Check if `left` is smaller or equal to `right`

```yaml
type: '<='
left: 20
right: 15
# Result: false, 20 is not greater or equal to 15
```

## Strings <a href="#strings" id="strings"></a>

Compare two strings

### Format <a href="#strings-format" id="strings-format"></a>

```yaml
type: operation # See below
left: string    # or placeholder that returns a string
right: string   # or placeholder that returns a string
```

### Equals (string equals) <a href="#strings-equals" id="strings-equals"></a>

Check if `left` is equal to `right` - **case sensitive**

```
type: string equals
left: Steve
right: steve
# Result: false, 'Steve' is not the same as 'steve'
```

### Equals ignore case (string equals ignore case) <a href="#strings-equals_ignore_case" id="strings-equals_ignore_case"></a>

Check if `left` is equal to `right` - **case insensitive**

```yaml
type: string equals ignore case
left: Steve
right: steve
# Result: true, 'Steve' is equal to 'steve'
```

### Contains (string contains) <a href="#strings-contains" id="strings-contains"></a>

Check if `left` contains `right` - **case sensitive**

```yaml
type: string contains
left: ArcaneVouchers
right: vouchers
# Result: false, 'ArcaneVouchers' does not contain 'vouchers'
```

### Contains ignore case (string contains ignore case)

Check if `left` contains `right` - **case insensitive**

```yaml
type: string contains ignore case
left: ArcaneVouchers
right: vouchers
# Result: true, 'ArcaneVouchers' contains 'vouchers'
```
