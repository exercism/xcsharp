# Instructions

In this exercise you're playing a role-playing game named "Wizard and Warriors" with your best friends. You are the Game Master, the person tasked with making the game world come alive for the players. A key aspect of this is describing the game to the players: what is a character's status, what the town they're visiting looks like, etc.

You have five tasks that have you describe parts of the game to the players.

## 1. Describe a character

Each character has a class, level and number of hit points and is described as: `"You're a level <LEVEL> <CLASS> with <HIT_POINTS> hit points."`. Implement the (static) `GameMaster.Describe` method that takes a `Character` as its sole parameter and returns its description.

```csharp
var character = new Character();
character.Class = "Wizard";
character.Level = 4;
character.HitPoints = 28;

GameMaster.Describe(character);
// => "You're a level 4 Wizard with 28 hit points."
```

## 2. Describe a destination

Each destination has a name and a number of inhabitants and is described as: `"You've arrived at <NAME>, which has <INHABITANTS> inhabitants."`. Implement the (static) `GameMaster.Describe` method that takes a `Destination` as its sole parameter and returns its description.

```csharp
var destination = new Destination();
destination.Name = "Muros";
destination.Inhabitants = 732;

GameMaster.Describe(destination);
// => "You've arrived at Muros, which has 732 inhabitants."
```

## 3. Describe the travel method

Characters can travel to a destination using one of two options:

- Walking, described as: `"You're traveling to your destination by walking."`
- On horseback, described as: `"You're traveling to your destination on horseback."`

Implement the (static) `GameMaster.Describe` method that takes a `TravelMethod` as its sole parameter and returns its description.

```csharp
GameMaster.Describe(TravelMethod.Horseback);
// => "You're traveling to your destination on horseback."
```

## 4. Describe a character traveling to a destination

When a character is traveling to a destination, this is described as a combination of the individual descriptions: `"<CHARACTER> <TRAVEL_METHOD> <DESTINATION>"`. Implement the (static) `GameMaster.Describe` method that takes a `Character`, a `Destination` and a `TravelMethod` as its parameters and return its description.

```csharp
var character = new Character();
character.Class = "Wizard";
character.Level = 4;
character.HitPoints = 28;

var destination = new Destination();
destination.Name = "Muros";
destination.Inhabitants = 732;

GameMaster.Describe(character, destination, TravelMethod.Horseback);
// => "You're a level 4 Wizard with 28 hit points. You're traveling to your destination on horseback. You've arrived at Muros, which has 732 inhabitants."
```

## 5. Describe a character traveling to a destination without specifying the travel method

In the majority of cases, characters are traveling to a destination by walking. For convenience, players are allowed to omit mentioning their travel method, in which case walking will be assumed to be the travel method. Implement the (static) `GameMaster.Describe` method that takes a `Character` and a `Destination` as its parameters and return its description.

```csharp
var character = new Character();
character.Class = "Wizard";
character.Level = 4;
character.HitPoints = 28;

var destination = new Destination();
destination.Name = "Muros";
destination.Inhabitants = 732;

GameMaster.Describe(character, destination);
// => "You're a level 4 Wizard with 28 hit points. You're traveling to your destination by walking. You've arrived at Muros, which has 732 inhabitants."
```
