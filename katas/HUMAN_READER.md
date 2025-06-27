# 👨‍💼HUMAN READER 📚

## Step 1

Given a number of seconds, be able to render it for humans. Then using 'years', 'months', 'weeks', 'days', 'hours', 'minutes', 'seconds'

⚠︎ Be careful with plurals

```
With 62 seconds,
Your function should return "1 minute and 2 seconds"
```

```
With 3662 seconds,
Your function should return "1 hour, 1 minute and 2 seconds"
```

```ruby
def to_human(seconds)
  # to implem
end
```

## Step 2

Given a number of whatnots and a "sizing contract", be able to render it for humans.

```
# With:
 - millimeters = 7 890 651 765,
 - contract: [
   - ["centimeter", 10], # 10 millimeters in a centimeter
   # who cares about decimeter ? :D
   - ["meter", 1000], # 1000 centimeters in a meter
   - ["kilometer", 1000], # 1000 meters in a kilometer
 your function should return "789 kilometers, 65 meters, 176 centimeters and 5 milimeters"
```

```
With:
 - bananas = 1401,
 - contract: [
   - ["box", 30], # 30 bananas in a box
   - ["pallet", 20], # 20 boxes in a pallet 
   - ["truck", 10], # 10 pallets in a truck
 your function should return "2 pallets, 6 boxes and 21 bananas"
```

```ruby
def to_human(whatnots, contract)
  # to implem
end
```

## Ideas to go further

- predefined contracts or custom ones

## Source

- [Human readable duration format](https://www.codewars.com/kata/52742f58faf5485cae000b9a)