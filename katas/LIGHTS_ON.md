# 💡LIGHTS ON! 💡

Welcome to the ACME company,
Our lights automatic switch-on when at least 1 employee is in the office. Otherwise, they switch-off.

## Goal

You must write a function returning the daily total minutes where lights were switch-on.

## Inputs

The employee flow in the office (employee name, entry time, exit time)

example:
```ruby
[
  ["Maurice", "09:00", "10:00"],
  ["Jeanne", "09:30", "10:30"],
  # ...
]
```

## Output

The total amount of minutes where lights were switch-on during the day

for the example above:
```
90
```

## Ideas to go further

- better format of the output (e.g. "1 hour and 30 minutes")
- another function listing the presence duration during the day per employee (sorted)
- validation to ensure the list is correct (e.g. if we have undetected employee entry/exits ; oversteps for a same employee)
- how many switching event (on or off) happened in the day?
