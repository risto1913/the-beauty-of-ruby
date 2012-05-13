## 1. What I have learned from Ruby

### * Just do as what you are thinking

In **Java** when you want to do something for 10 times, the code will be :

``` java
for(int i = 0; i < 10; i++){
  // do something
}
```
this is not the way you think, it's the way of computer's

In **Ruby**, we use the following code :

``` ruby
10.times{ # do something }
```

this is a very basic example, let's take another example. (_we will continue compare Java to Ruby, because I was a Java developer before_)

### * Things should act as what they should be

In **Java** when you want to call a attribute of a class instance, the code will be : 

``` java
class Person{
  public String name = "I am the person";
}

Person me = new Person();
me.name; // => I am the person
```
of course the code is not good, you will say , we need get/set method to keep things under control. OK. The code will be :
``` java
class Person{
  private String name = "I am the person";

  public void setName(String name){
    this.name = name;
  }
  
  public String getName(){
    return this.name;
  }
}

Person me = new Person();
me.getName(); // I am the person
me.setName("changed");
me.getName(); // changed
```
I really thanks Java, compare to Java, Ruby is really a Ruby. Let's see the Ruby way, hold your breath : 
``` ruby
class Person
  attr_reader :name
  
  def initialize
    @name = "I am the person"
  end
  
  def name=(name)
    @name = name
  end
end

me = Person.new
me.name # => I am the person
me.name = "changed"
me.name # => changed
```
I don't want to say the code is less than Java. What I want to point is when I want to get a person's name, 
I just use `me.name` and when I want to set a person's name, I just use `me.name = "changed"` in Ruby, and they are
still under control. if people who use your code as api, he only needs to know, there is an attribute called `name`, 
not 2 methods called `getName(String name)` and `setName()`. _They are still methods, but they act like attibutes_
