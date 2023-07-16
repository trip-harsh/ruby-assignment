# Question 1:

In Ruby, implicit blocks are a convenient way to pass a block of code to a method without explicitly using the `do` and `end` keywords or the curly braces `{}`. Implicit blocks are often used in methods that expect a block to be passed for customizing their behavior. Here's an example to illustrate the usage of implicit blocks:

```ruby
def fun 
  puts "lets start"
  yield if block_given?
  puts "End"
end

fun {
  puts "Started";
}
```

Output:
```
lets start
Started
End
```

# Question 2:

```ruby

def hello(a, proc_greet)
  
  str = proc_greet.call(a)
  puts str
  
end

proc_greet = Proc.new{|name| "Hello #{name}"}

hello("Harsh", proc_greet)

```

OUTPUT:

```

Hello Harsh

```

# Question 3:

Blocks, Procs, and Lambdas are all features in Ruby that allow us to define reusable chunks of code. However, they have some differences in terms of syntax, behavior, and how they handle arguments. Here's a breakdown of the differences:

Blocks:
- Blocks are not objects in themselves but rather chunks of code that can be passed to methods.
- Blocks are defined using either curly braces `{}` or the `do...end` keywords.
- Blocks are usually used implicitly with methods that accept them, such as iterators.
- Blocks cannot be saved as variables or passed around independently.


Procs:
- Procs are objects that encapsulate blocks of code.
- Procs are created using the `Proc.new` or `proc` methods, or by using the `->` (stabby lambda) syntax in Ruby 1.9 and later versions.
- Procs can be saved as variables, assigned to constants, and passed around as objects.
- Procs are invoked using the `call` method.


Lambdas:
- Lambdas are also objects that encapsulate blocks of code.
- Lambdas are created using the `lambda` keyword or the `->` (stabby lambda) syntax.
- Lambdas can be saved as variables, assigned to constants, and passed around as objects.
- Lambdas are invoked using the `call` method or by using the lambda syntax `lambda.(args)` or `lambda[args]`.

# Question 4:

```ruby

def check?(str)
  i = 0
  j = str.length()-1
  
  while i < j
    if str[i] != str[j]
      return false
    end
    
    i+=1
    j-=1
  end
  
  return true
end

puts check?("aabbaa")
puts check?("hello")

```

# Question 5:

```ruby

arr = [1,2,3,4,5,6,7,8]

maxi = arr.max
mini = arr.min

puts (maxi+mini)

```
