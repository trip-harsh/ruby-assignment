# Question 1:

```ruby

for i in 1..100
    
    if(i%2 != 0)
        puts i
    end
    
end

```

# Question 2:

```ruby

def solve(arr)
    
    dict = {
        1 => "Monday",
        2 => "Tuesday",
        3 => "Wednesday",
        4 => "Thursday", 
        5 => "Friday",
        6 => "Saturday",
        7 => "Sunday"
    }
    
    ans = arr.map { |day| "#{day}-#{dict[day]}"}.join(", ")
    return ans
    
end


arr = [1,5,7,4,2,6,1,4,2,7]

puts solve(arr)

```

# Question 3:

```ruby

def sort(arr)
    
    n = arr.length()
    
    for i in 0...n
        for j in i...n
            if(arr[i] > arr[j])
                temp = arr[i]
                arr[i] = arr[j]
                arr[j] = temp
            end
        end
    end
    return arr
    
end


arr = [12,15,9,4,30,3,7]

arr = sort(arr)

puts arr

```

