#bash #text-processing #terminal #tool #helper 
Command-line JSON processor.
# Quick examples
```
[
  {
    "name": "John",
    "age": 30,
    "address": {
      "city": "New York",
      "state": "NY"
    }
  },
  {
    "name": "Jane",
    "age": 25,
    "address": {
      "city": "Los Angeles",
      "state": "CA"
    }
  }
]


# jq Cheatsheet

# Basic Usage
jq . file.json                          # Read a JSON file
echo '{"name": "John", "age": 30}' | jq .  # Read JSON from a string

# Selecting Data
jq '.name' file.json                    # Select a specific key
jq '{name: .name, age: .age}' file.json # Select multiple keys
jq '.address.city' file.json            # Select nested keys

# Filtering Data
jq '.[] | select(.age > 25)' file.json  # Filter based on a condition
jq '.[] | select(.age > 25) | {name: .name, age: .age}' file.json # Filter and project

# Modifying Data
jq '. + {gender: "male"}' file.json     # Add a new key
jq '.age = 31' file.json                 # Update a key
jq 'del(.age)' file.json                 # Delete a key

# Working with Arrays
jq '.[]' file.json                       # Select all elements in an array
jq 'length' file.json                    # Get the length of an array
jq 'map(.name)' file.json                # Map over an array

# Combining Filters
jq '.[] | {name: .name, age: .age} | select(.age > 25)' file.json # Combine filters with |
jq '.name, .age' file.json               # Use , to combine results

# Output Formatting
jq '.' file.json                         # Pretty print JSON
jq -r '.name' file.json                  # Output as raw strings

# Saving Output
jq '.' file.json > output.json           # Save output to a file

# Common Options
jq -c '.' file.json                      # Compact output
cat file.json | jq .                     # Read from stdin
jq -f filter.jq file.json                # Use a filter from a file
```