

Some notes to help your navigation here:

1. I have used features to specify what the system should do.
2. Then I proceeded to the implementation.
3. I have defined two pricing rules. See the `models/pricing_rules` directory. One can define others too. Checkout will not
be changed.
4. The `Checkout` class has the `#initialize`, `#scan` and `#total` methods as per the requirements.
5. You can run `bundle exec cucumber` to see the test running green.
6. You can also use the `bundle exec ruby main.rb` to run an interactive Ruby program that asks for products to be added
to the basket and then does the checkout.