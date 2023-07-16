# Question 1:

```ruby

dict = {}

arr = [1,2,3,2,5,6,9,6,5,3,2,2,1,8,10,10,7]

for i in arr
  if dict.include? i
    dict[i] += 1
  else
    dict[i] = 1
  end
  
end

puts dict

```

# Question 2:

```ruby

sum = 0

for i in 100..200
  sum += i
end

puts sum

```

# Question 3:

```ruby

def div(a, b)
  begin
    c = a/b
    puts "a/b = #{c}"
    
  rescue ZeroDivisionError
    puts "Division by zero not allowed!!"
  end
end


puts div(1,4)
puts div(2,0)

```

# Question 4:

```ruby

def solve(s, target, new_val)
  ans = s.chars.map{|char| char == target ? new_val : char}.join()
  return ans
end


puts solve("Hekko I am Harsh", 'k', 'l') #Output: Hello I am Harsh

```

