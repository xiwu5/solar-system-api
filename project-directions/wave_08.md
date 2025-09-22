# Wave 08: One-to-Many Relationships

We want to practice one-to-many relationships similar to what we've seen in the Hello Books API. To do this we will:
1. Add a Moon model
2. Create a one-to-many relationship between the Planet and Moon models 
3. Add nested routes for the endpoint `/planets/<planet_id>/moons` to:
    - Create a Moon and link it to an existing Planet record
    - Fetch all Moons that a Planet is associated with

## Create a Moon Model

1. Create a Moon model with attributes `size` and `description`, and at least one other attribute you choose together.
2. Make a foreign key connection between Planet and Moon models using `back_populates` to create a bidirectional relationship. [SQLAlchemy docs on one-to-many](https://docs.sqlalchemy.org/en/20/orm/basic_relationships.html#one-to-many)
    - Make sure to create and run migrations as the models change, and to commit those files so your teammates can access them as well!
    - For testing, you may want to update the Planet’s `to_dict` function to return info about their moons, if they exist. 

## Create Nested Routes

1. Create a nested route for `/planets/<planet_id>/moons` using the POST method which allows you to add a new moon to an existing planet resource with id `<planet_id>`.
    - Make sure to test out your new route in a browser or Postman before continuing!
2. Create a nested route for `/planets/<planet_id>/moons` with the GET method which returns all moons for the planet with the id `<planet_id>`.

If you finish and have more time, take a look at what else could be refactored or discuss what other nested endpoints you think would be helpful!
