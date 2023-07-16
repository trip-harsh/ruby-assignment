# Question 1:

```ruby

def check?(email)
    
    pattern = /^[A-Za-z]\w*(@)(\w+\.)[a-zA-Z]{1,4}$/
    
    return email.match?(pattern)
end

puts check?("invalid@domain")
puts check?("test@example.com")

```

# Question 2:

```ruby

class Vehicle 
  def initialize 
     puts "I am a vehicle"
   end 
 
   def max_speed 
     puts "10"
   end 
 end 
 

class Car < Vehicle
  def max_speed
    puts "100"
  end
end

class Rickshaw < Vehicle
  def max_speed
    puts "25"
  end
end

obj = Car.new
obj.max_speed

onj2 = Rickshaw.new
onj2.max_speed
  
```

# Question 3:

In Ruby, both modules and mixins are important features that provide code reuse and help organize and extend functionality. However, there are differences between modules and mixins in terms of their intended use and how they are included in classes.

Module:
- A module in Ruby is a container for a set of methods, constants, and other module-level definitions.
- Modules cannot be instantiated or directly used to create objects.
- Modules are typically used as namespaces to organize related methods or to provide a way to share common functionality across classes.
- Modules can be included in classes using the `include` keyword, allowing the class to access and use the methods and constants defined in the module.

Mixin:
- A mixin is a module that is designed to be included in a class, providing additional behavior and extending the class's functionality.
- Mixins are used to implement multiple inheritance-like behavior in Ruby.
- When a mixin is included in a class, the class gains access to all the methods and constants defined in the mixin.
- A class can include one or more mixins, allowing it to incorporate functionality from multiple sources.

In summary, modules are primarily used for organizing code and sharing functionality, while mixins are modules specifically designed to be included in classes to extend their behavior and provide additional functionality. Mixins enable multiple inheritance-like behavior, allowing classes to incorporate functionality from multiple sources without the limitations of traditional inheritance.

# Quesion 4:

In Ruby, private and protected methods are used to control the visibility and accessibility of methods within a class hierarchy. Here are the key differences between private and protected methods:

Private Methods:
- Private methods in Ruby can only be called within the context of the defining class. They cannot be accessed by instances of the class or its subclasses.
- Private methods cannot be called with an explicit receiver, meaning they cannot be invoked using the dot syntax (`obj.private_method`). They can only be called implicitly within the class itself, typically from other methods within the same class.
- Private methods are typically used for internal implementation details or helper methods that are not intended to be exposed to external code.
- In Ruby, you can declare a method as private by using the `private` keyword followed by the method names, or you can group multiple method definitions under a single `private` block.

Protected Methods:
- Protected methods in Ruby can be called within the context of the defining class or its subclasses. They are accessible to instances of the class and its subclasses.
- Protected methods can be called with an explicit receiver, meaning they can be invoked using the dot syntax (`obj.protected_method`), allowing subclasses to access and invoke them.
- Protected methods are typically used when you want to restrict access to certain methods within a class hierarchy but still allow subclasses to access and use them.
- In Ruby, you can declare a method as protected by using the `protected` keyword followed by the method names, or you can group multiple method definitions under a single `protected` block.

To summarize, private methods are only accessible within the class that defines them and cannot be invoked explicitly using a receiver. Protected methods, on the other hand, can be accessed by instances of the class and its subclasses, and they can be invoked explicitly using a receiver.
