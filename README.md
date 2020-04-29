# Upgrade your Ruby CLI Project

It has probably been a little while since you looked at your first portfolio
project, the Ruby CLI app. Now is a good time to revisit it and read the code
you've written. Since it was early on in your journey with Flatiron, it is
you've likley improved your coding skills. Although this project may not be as
visually appealing as other portfolio projects, with some upgrades and polish,
it can still be a good example of what you can accomplish. Below are some
suggestions for what you can do to upgrade your CLI project.

## Refactor

As mentioned, you're likely better at coding now than you were when you created
this project. Put these skills to use! Read through your project's code and consider some of these questions:

- **Is the code DRY? Is there any redundant content that could be reduced or
  abstracted?** Under time constraints, it is easy to forgo the
  [Don't Repeat Yourself][] principle. There is no due date anymore, though, so
  take some time to clean up any repetitive patterns in your code.
- **Can you spot and unnecessary or overly complicated code?** While learning the
  basics, it is possible to misunderstand how specific code works. Sometimes, we try
  things until something sticks. Sometimes, the moment a piece of code works, we move on to the next task without reconsidering what we've written. Now is the time to look back and find examples of this in your project.
  
One common mistake we make when first learning to code is to use extra variables
and steps that are either unused or not necessary. Check the variables in your
code. Are the values they contain used later on? Can they be removed with
minimal changes? Consider the example below:

  ```ruby
  def example_method(parameter)
    variable = parameter
    result = another_method(variable)
    result
  end
  ```

Both `variable` and `result` are unnecessary. This method could be rewritten
without them:

  ```ruby
  def example_method(parameter)
    another_method(parameter)
  end
  ```

Sometimes, once we've cleaned up our code, it becomes easier to spot unnecessary
steps. In the example above, after removing the extra variables, it is clear
that this method is just calling another method. We could possibly just remove
`example_method` entirely, and instead just use `another_method` directly.

Another common mistake - stuffing too much into a single method. For readability
and flexibility in our code, it is good to make sure methods are not overly
complicated. Methods should typically do one task. That task may be to compute a
value or transform a piece of data. It may even be that a method exists purely
to call a few other methods in a specific order. The fewer tasks a method
completes, the easier it is to understand what it does. This also makes methods
more useful. For instance, if you have a single method that both calculates
_and_ transforms some data, by splitting up the tasks, you will have two
methods, one that calculates and one that transforms. Functionally, this won't
change what the program does. However, now you have two methods that can be
reused elsewhere individually.

**Remember:** Refactoring is about cleaning up your code **without** changing
functionality. After refactoring, your application should do exactly what it did
before, but the code should be more efficient and easier to read.

[Don't Repeat Yourself]: https://en.wikipedia.org/wiki/Don%27t_repeat_yourself

## Finish and Add Features

Many students don't get to finish every feature they think of for their
projects. Portfolio projects are often at the [MVP stage][]. They are functional
but there is so much more that can be done to make them better.

Think about what features could be added to your CLI project. In particular, what
can be added to make the project more interesting to potential employers? Some
things to consider:

- Are there any 'dead-ends' in your project? Maybe you started to add a feature,
  but closed it off due to time constraints. Can this feature be added? If
  you're not going to add that feature, are there parts of your code that are
  half-implemented and can be removed?
- Can you augment your project with APIs? Or if it already uses an API, can that
  API be used to expand functionality?

[MVP stage]: https://en.wikipedia.org/wiki/Minimum_viable_product

## Polish and Document

If you intend to share your CLI project with potential employers, try and think
about what the project may look like to those employers. Run your project and
play through the possible ways someone could use it. If an employer were to
clone down your project and try to run it, are there steps in the process that
are not obvious? Can you add functionality to make the project easier to
understand and use?

One example would be to add `help` functionality - built-in documentation on how
to navigate the project. This helps prevent potential users from misusing or
misunderstanding the project. It also shows that you've thought a bit about the
user experience.

In addition, we also recommend writing some documentation for the project and
storing it in a `README.md` file. This documentation should include instructions
for setting up the project and what dependencies, if any, the project relies on.
It can also include context that will help frame your project. Maybe you built
it with the intention of solving a specific problem. Include this in the
`README.md`.

## Deploy as a Ruby Gem

CLI projects can be tricky to showcase. They usually require some setup to get
working that may not be obvious to a potential user. One great way to get around
this is to make your project into a Ruby Gem.
[Check out this guide from rubygems.org on how to create a gem][gem guide].
Hosting gems on [Rubygems.org](https://rubygems.org/) is free and is a great way to
supercharge your CLI project, converting it from a personal project to a useful
tool that others can easily use. Instead of requiring someone to clone down a repo,
they'll be able to quickly try your project out with the `gem install` command.

[gem guide]: https://guides.rubygems.org/make-your-own-gem/

## Conclusion

At the end of our courses, students often lean towards showcasing their later
JavaScript and React projects. This makes sense - these projects have benefitted
from our improved understanding of programming. They often have more features
and they look more visually appealing.

Having a good, functioning CLI project, however, can augment your list of
accomplishments. It shows you are versatile. As a software engineer, you will
sometimes find yourself in need of custom tools to complete the work you do.
However you choose to upgrade your CLI project, this is a great opportunity to
showcase your ability to build solutions to the challenges you'll face.