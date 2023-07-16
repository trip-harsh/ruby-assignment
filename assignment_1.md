# Question 1:

```ruby

class Circle
    
    attr_accessor :radius
    
    def initialize(radius)
        @radius = radius
    end
    
    def getArea
        return 3.14 * radius * radius
    end
    
    def getCircumference
        return 2 * 3.14 * radius
    end
    
end

obj = Circle.new(5)

# Area
puts obj.getArea

# Circumference
puts obj.getCircumference

```

# Question 2:

```ruby

num = 9.312482

s = format("$%.2f", num)
puts s

```

# Question 3:

```ruby

class Temperatue
    
    def convertFahrenheit(temp)
        puts (temp * 9/5) + 32
    end
    
    def convertCelsius(temp)
        return (temp - 32) * 5/9
    end
    
end


obj = Temperatue.new

# 1
puts obj.convertCelsius(98)

# 2
obj.convertFahrenheit(32)

```
