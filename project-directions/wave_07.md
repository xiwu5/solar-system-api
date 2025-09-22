# Wave 07: Refactoring

## Refactor Models & Routes

Update the `Planet` model with similar refactors presented in the Hello Books API:

In the `Planet` model:
1. Create an instance method `to_dict`
2. Create a class method `from_dict`

In a new file:
1. Create a function that handles generalized id validation for models.

In the `planet_routes` file:
1. Update routes that fetch planet data to use the new instance method `to_dict` when creating a dictionary representation of a planet
2. Update the create planet route to use the new `from_dict` class method to create new planet instances.
3. Update any routes that need to validate a model's id to use the new generalized id validation helper function

The behavior of our routes should stay the same through these refactors. We should not see any changes to the capabilities our routes had previously.