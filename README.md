# A coding exercise

A supermarket sells only 3 products:

```
+--------------|--------------|---------+
| Product Code |     Name     |  Price  |
+--------------|--------------|---------+
|     FR1      |   Fruit tea  |  $3.11  |
|     AP1      |   Apple      |  $5.00  |
|     CF1      |   Coffee     | $11.23  |
+--------------|--------------|---------+
```

Supermarket CEO is a big fan of buy-one-get-one-free offers and of fruit tea. He wants us to add a rule to do this.

The COO, though, likes low prices and wants people buying apple to get a price 
discount for bulk purchases. If you buy 3 or more apples, the price should drop to $4.50.
Our check-out can scan items in any order, and because the CEO and COO change 
their minds often, it needs to be flexible regarding our pricing rules.

The interface to our checkout looks like this (shown in Ruby):

```
co = Checkout.new(pricing_rules)
co.scan(item)
co.scan(item)
price = co.total
```

Implement a checkout system that fulfils these requirements in Ruby.

Here are some test data:

```
Basket: FR1, AP1, FR1, CF1
Total price expected: $19.34
```

```
Basket: FR1, FR1
Total price expected: $3.11
```

```
Basket: AP1, AP1, FR1, AP1
Total price expected: $16.61
```

# Implementation

Some notes to help your navigation here:

1. I have used features to specify what the system should do.
2. Then I proceeded to the implementation.
3. I have defined two pricing rules. See the `models/pricing_rules` directory. One can define others too. Checkout will not
be changed.
4. The `Checkout` class has the `#initialize`, `#scan` and `#total` methods as per the requirements.
5. You can run `bundle exec cucumber` to see the test running green.
6. You can also use the `bundle exec ruby main.rb` to run an interactive Ruby program that asks for products to be added
to the basket and then does the checkout.