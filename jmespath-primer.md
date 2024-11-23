# JMESPath Primer

Using the ```--query``` feature in the az devops cli is very alien at first. Here's a quick primer.

## Basic Queries

Let's assume we have a simple JSON structure:

```json
[
  {
     "name": "Bryan",
     "fruit": "Orange",
     "car": "SUV"
  },
  {
     "name": "Mark",
     "fruit": "Banana",
     "car": "Sedan"
  }
]
```

**Return the first element**: ```"[0]"```

```json
{
   "name": "Bryan",
   "fruit": "Orange",
   "car": "SUV"
}
```

**Return the name element of first element**: ```"[0].name"```

```json
{
   "name": "Bryan"
}
```

**Return multiple elements**: ```"[0].{Name:name, Car:car}"```

```json
{
   "Name": "Bryan",
   "Car": "SUV"
}
```
