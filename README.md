# How To Find Gems

## Objectives

1. Understand what to look for when choosing a gem.
2. Know where to find popular gems.

## The RubyGems Ecosystem

We've been using gems like crazy at this point, from RSpec for testing
to Rails for ... Rails-ing. Almost any general problem we need to solve
has already been solved by someone else and released as a gem, allowing
Ruby and Rails developers to reach incredible levels of productivity
because we get to skip all that wheel-reinventing that Java
programmers do all day.

**//Flat-fact:** Reinventing wheels is actually what Java programmers do
as a side hustle while they're waiting for compiles.

Working in Ruby is such a joy not just because of the language itself,
but also because of the people who freely give back to their fellow
developers in the form of gems.

## Do I Even Need A Gem?

The wealth of gems (pun absolutely intended) available for everyone to
use in their projects is one of the things that sets Ruby apart from
other languages, but it can also lead to *Gem Madness* - a condition
where gem-crazed developers look for a gem to solve every problem
without considering if a gem is really needed.

**//Flat-fact:** Gem Madness is not currently listed in the DSM-V as an
official disorder, but we should all work to raise awareness.

Before we go looking for a gem to solve a problem, we should take a
little time to decide if the problem we want to solve is really so big
that we need a gem, or if we might be able to figure out (or Google) a
way to just write the code ourselves.

## Where To Look

Okay, we know we need a gem, where do we find one?

We can actually look for gems right on our command line. Try this out in
your console:

`gem search ^twitter$ -d`

The `gem search` command can take a regular expression and can be very
handy if you know the name (or part of the name) of a gem and want to
find it quickly.

However, that only searches the name, so if you need to search in a
little more open way, the obvious choice is Google. A search of `rails
gem problem-description` will probably get you there pretty quick.

Google, however, isn't great at letting us know if we want the gem it
shows us (more on this later), so there's a couple of great resources
that provide more context to lists of gems.

[Ruby Toolbox](https://www.ruby-toolbox.com/) is a site that aggregates
and categorizes gems, and ranks them according to stats like total
downloads, releases, and active commits.

Ruby Toolbox is *comprehensive*, which is a fancy way of saying "it's
kind of a lot". Great if you're looking for something a little more
obscure, or really want to explore all the options, but sometimes we
want a more curated list of what gems are popular in the community.

Enter [Awesome Ruby](https://github.com/markets/awesome-ruby) and
[Awesome Rails Gems](https://github.com/hothero/awesome-rails-gem), two
open-source, community maintained lists of the most popular gems for
Ruby and Rails by category.

**Note:** There are "Awesome" lists for a lot of things, from languages
to free programming books and everything in between. Check out the
[index](https://github.com/sindresorhus/awesome).

## Qualities To Look For When Choosing A Gem

Adding a gem to your project means you are taking on a
*dependency* on outside code. If that gem has security problems, your
project has security problems. If that gem has bugs, your project has
bugs. If that gem doesn't keep up with newer versions of Rails, or even
of the gems that it might use itself, you might be stuck dealing with
compatibility problems.

So let's look at some strategies for selecting high quality, reliable,
and safe gems for our project.

### How Popular Is It?

This is one time when we want to care about popularity contests. The
more popular a gem is, the more likely it is to be maintained, to keep
up with security issues, and new Rails versions.

Beyond that, the more popular a gem is, the more likely you are to be
able to find help if you run into problems. Popular gems have a lot of
questions and answers on StackOverflow. People like to blog about
popular gems so they can get those sweet sweet clicks. All that adds up
to you feeling confident that you can use that gem.

Some ways to test the popularity are:

1. Look it up on Ruby Toolbox. See how many downloads there are, how
   recently it's been committed to, and how many versions there are.
2. See if it's on the Awesome Ruby or Awesome Rails lists mentioned
   above.
3. Google the gem name and see what's there, and, importantly, how
   recent it is. Try things like "gem name tutorials" and "gem name
errors".
4. Search StackOverflow for the gem and read what people say about it.
5. Seach Github for usage of the gem. You'll need to read the gem's
   documentation or code and pick out a class or method to search for.
For example, searching Github for `has_attached_file`, which is a
primary method in the [Paperclip](https://github.com/thoughtbot/paperclip) gem yields over 100K results, so it's obviously in wide use.

### How Well-Maintained Is It?

We want our gems to be popular, but we also need them to be
well-maintained. A well-maintained gem will be far less likely to cause
you problems down the road.

Some ways to determined if a gem is well-maintained are:

1. Read the code. Is it put together in the way you'd expect? Can you
   understand it? Does it follow Ruby idioms and styles?
2. Look for documentation. Is it well-documented? The README, at a bare minimum, should tell you
   how to get up and running. Even better if there's a wiki with
examples and sample code.
3. Look at issues and pull requests. How long do they stay open? How
   active are the committers in addressing issues and PRs? Are there
problems with a specific version that haven't been resolved.
**Hint:** This could also be an opportunity to do some open source
contributing!
4. Look for tests. Is there a `/test` or `/spec` directory? How many
   tests are there? Is there a link to a continuous integration build result? Examining the tests is always a great way to learn how the gem works and how well it's put together.

## Summary

Gems are great. They're a powerful tool and crucial to your success as a
Ruby on Rails developer. But just because there's a gem out there for
everything, doesn't mean that every gem is the best one to use, so do
some due diligence when choosing what to add to your Gemfile.

![Gem](http://i.imgur.com/6ipUqve.gif)
