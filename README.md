# FINAL PROJECT - Building a Fake Grab Food

## Introduction

Welcome to the Final Project during our course. Since we have begun the whole process of this course for this project, I have now glad to present you our final project with the description below.

## Background

When I get hungry, I want to `find` somewhere to eat.
Sometimes, I `crave` Vietnamese food, sometimes England, sometimes Thailand, sometimes Sushi
My craving can be `influenced` by anything, including ads on the radio or on TV, driving by a particular place, or even by random events
For example, France is playing in the World Cup today... maybe I'll root for the French... French toast... I should go to a diner to get french toast soon!) I like to eat at new places, but only if it comes recommended, particularly by a friend, or a friend of a friend (etc.). That way I can share my experience after the meal ("Dude, the paella was AWESOME!"), or complain about the meal.

## Specification

For this assignment, you will design a data structure to respond efficiently to the operations in the following list

-   CREATE `username`

Adds a new user with name `username` to the system. The `username` may not contain whitespace. Anything after the first string of non-whitespace characters should be ignored by your program. If the user enters a duplicate `username`, your program should disallow it, print an error message to match our sample executable (coming soon!), and continue.

-   FRIEND `username1` `username2`

Records that `username2` is a friend of `username1`

-   UNFRIEND `username1` `username2`

Records that `username2` is no longer a friend of `username1`. Whether or not `username1` is a friend of `username2` remains unchanged by this command.

-   ADD `restaurant-name` `cuisine`

Adds a new restaurant named `restaurant-name`, which serves cuisine of type `cuisine`. For example, the user may enter "ADD LittleVenice Italian" or "ADD ParkwayDiner Breakfast". A restaurant may serve only one type of cuisine in our system. ("You know what would be great?"...)

-   REC `username` `restaurant-name`

Records that `username` recommends restaurant `restaurant-name`. Recommending a restaurant is a binary thing... you either recommend it or you don't... no 3.5 stars. If `username` already recommends `restaurant-name`, then this command has no effect and your program should simply continue.

-   UNREC `username` `restaurant-name`

Records the fact that `username` no longer recommends restaurant `restaurant-name`. If `username` had not recommended `restaurant-name` prior to this command, the the command has no effect.

-   CRAVE `username` `cuisine` `points`

Tracks `username`'s eating mood, to add `points` points to that user's current taste for cuisine `cuisine`. For example, if someone mentions pizza within earshot of me, then I'm going to be a little more inclined to want pizza for lunch. Maybe that's modeled as "CRAVE Mike pizza 10". If someone says the snow is likely to melt today, I might immediately think of melting cheese, which makes me think of pizza, and that could be modeled with "CRAVE Mike pizza 15". Then I would have 25 "pizza craving points". But right after that I might see five guys walking down the street and might immediately be in the mood for a burger... "CRAVE Mike burger-joint 20". The mind of a hungry professor works in mysterious ways.

-   EAT `username` `friendship-distance`

When it's time for `username` to eat, we enter this command, and the system tells that user where to eat, as follows:

Whichever cuisine `username` currently craves the most will be selected by your program as the type of restaurant at which to eat.
Your program will then find a restaurant that "is recommended" by `username`'s friendship network.
If `friendship-distance` is set to 1, then the selected restaurant must serve `cuisine` cuisine, and be recommended by someone who `username` considers a friend. If `friendship-distance` is set to 2, then the selected restaurant may be recommended by a friend of a friend (but still must serve `cuisine` cuisine). If `friendship-distance` is k, then the selected restaurant must be "within k friendships". But in all cases, the selected restaurant must be the "closest" (in terms of number of friendships away) restaurant that serves the specified cuisine. That is, if restaurant A serves Italian food and is recommended by a friend of a friend, and restaurant B serves Italian food and is recommended only by a friend of a friend of a friend (but not by a friend or by a friend of a friend), then restaurant A must be selected before restaurant B, even if `friendship-distance` is set to 3.

If no restaurant that serves `cuisine` cuisine is within `friendship-distance` friends away, then this command should display an error to match the sample executable (coming soon!), and continue.

Once `username` eats at a restaurant that serves `cuisine` cuisine, then the points for that cuisine, for that user, should be set back to 0.# Final-Project
