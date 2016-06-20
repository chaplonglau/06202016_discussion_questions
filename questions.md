1. Think about arrays
- What are some of the methods (non-iterator methods) that you know? 
   Length, sort, uniq, flatten

- When are they used?
    Length= get the length of the array
    Sort= sort it alphabetically
    Uniq= returns an array with removed duplicates
    Flatten= 1-D it 


2. Now list iterator methods for arrays
- There are four main ones that we have discussed
    Each, select, collect, map

- When do you use each one
    Each=no modification
    Select= find only values relevant
    Collect= returns modified array
    Inject=returns result of last iteration 


3. Now onto objects
  1. Why do we even have objects?  Why not just use hashes?
    Objects have properties and interact with other objects, hashes hold data and usually do not interact with other hashes.
  2. What is the difference between using a getter method, and just referencing the instance variable?
    @name vs get_name. in OOP, we don't want the user to be messing with private variables. get_name is preferred. 

  3. Should a method that finds the correct user by name (eg. find_by_name?) be a class method or instance method?  Why?
    class method, because you're looking for an instance of a class. 
  4. How does initialize work in an object?
    it corresponds with new. 
  5. What two methods will attr_accessor :name write?
    def name=@name
    def name= (name) @name=name

4. Object Relations
  Consider books, authors and genres.
  1. Draw out the relations between the objects.  Assume a book can only have one genre.
    Authors has many books
    Authors has many genres
    Genres has many books. 
  2. Which object is going act as my join - and thus store the data?
    Books 
  3. Ok, now write out the three classes and fill in the belongs to relations.
    Book belongs to author
    Book belongs to genre
  4. Now write the method that will give me a list of books written by an author.
     artists.books 
     SELECT titles FROM books JOIN authors ON books.author_id= authors.id 
  5. Now write a method that will give a list of all of the genre's of an author.
      author.genres 

      SELECT authors.name, genres.name FROM authors INNER JOIN books ON authors.id=books.author_id INNER JOIN genres ON genres.id =books.genre_id WHERE authors.id="2";
