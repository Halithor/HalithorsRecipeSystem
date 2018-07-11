# Halithor's Recipe System
This system provides a generic way to register items and recipes in for custom
maps made for Warcraft III using the [Wurst language](https://wurstlang.org/). 

### Features

- Item stacking and stack splitting support
- Define crafting recipes in a single line!
- Supports efficient automatic crafting (the system intelligently picks the right recipes)
- Recipes can be shaped (specific slot requirements) or unshaped
- Recipes support counted ingredients

# Usage
Everything is setup via the configuration file which the user provides. Direct 
calls to the recipe system will be done through `unit.craftRecipe()` and similar functions. 

### Configuration
Create a file named `RecipeSystemConfig_config.wurst` and implement the functions `registerItems()` and `registerRecipes()`. Use the methods named `registerItem` to register items in the system. Registering items in the system allows the system to know their names and stack the item type. Use `registerRecipe` to register a recipe with a given product. The helper methods `asIngredients` and `asIngredientsOrdered` create ingredient lists for recipe from the arguments provided, the first being shapeless and the second being shaped (specific slot ingredient reqs).

# Example
See my example in this repository: [Halithor's Recipe System Demo](https://github.com/Halithor/HalithorsRecipeSystemDemo). The configuration file is an example of setting up some items and recipes in the system. The demo file contains item definitions and the map initialization.

# Planned Features

- Recipes with multiple, counted products
- Partial recipe completion: recipes that can take many resources
- "Recipe books" based on the recipes defined. Easy text tools
- Configuration for abilities causing recipe attempts

