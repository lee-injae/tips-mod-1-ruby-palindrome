## Palindrome Solution

### Built-in Methods Solution
```ruby
  def palindrome?(string)
    string == string.reverse
  end
```

### Iterative Solutions
```ruby
def palindrome?(string)
 string.length.times do |i|
  if char[i] != char[-(i+1)]
   return false
  end
 end
 true
end
```

```ruby
def palindrome?(string)
  left = 0
  right = string.length
  
  # run it for only half the string so the indices
  # don't cross over and double-check things
  while left < right
    if string[left] != string[right]
      return false 
    end 
    left += 1
    right -= 1
  end
  true
end
```

### Recursive Solution

``` ruby
  def palindrome?(string)
    if string.length == 1 || string.length == 0
      true
    else
      if string[0] == string[-1]
        palindrome?(string[1..-2])
      else
        false
      end
    end
  end
```
