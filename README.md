# mini-amazon-cs316

**MINI-AMAZON**
Visit at http://better-amazon.colab.duke.edu:5000/ (Not currently running)

**How to run (Paul's method, assuming Mac):**

1. clone and cd into folder
2. run `python3 -m venv test-venv` (if test-venv does not already exist)
3. `source test-venv/bin/activate` (this will activate the virtual environment)
4. `pip install -r requirements.txt` (installs dependencies)
5. `export FLASK_APP=app.py` (exports the main flask app)
6. **If running locally** `flask run` and go to local url provided  
**If running on VM** `flask run --host 0.0.0.0` (inside `tmux`), then navigate to http://better-amazon.colab.duke.edu:5000/ 

NOTE: if on VM, the app may already be running. If so, you may need to:
 - run `ps -a` which will list running processes
 - get the pid of whichever process is listed as Flask
 - `kill [pid]`
 
 # Project Description
This project is a simplified version of Amazon’s website. By configuring a frontend that
mimics Amazon’s shopping experience while maintaining a backend that stores information
about users and site content, we have created a site that functions very similarly to Amazon. In
total, we have four different types of accounts: users, sellers, warehouse managers and a singular
administrator account. Our site allows users to browse items, add items to their cart, and check
out all while keeping track of that user’s information and the delivery status of their purchased
items. It also allows for people to have seller accounts from which they can list items for sale and
manage their listings. Our site has an added functionality for warehouse managers who can make
accounts to manage the deliveries of their warehouse and see their past order history as well. The
administrator account allows someone to manage the entire site and database.
To accomplish this, we leveraged the power of Flask, a Python based microframework
for web applications, to create both the frontend and the backend. Flask has a variety of powerful
extensions and supports Python’s existing packages, such as SQLAlchemy, Python’s SQL
toolkit. This greatly simplified the process of building the web application. 

# Contributions
Amr Bedawi worked on all aspects of the login page, the signup page, and the forgot password
page. Olivia Leggio worked on the base HTML/CSS for the top bar, the account page, the cart
(involving checking out items and removing them), the account balance page, and the order
history page. Paul Sabharwal worked on the initial SQLAlchemy setup and schema declaration,
importing the ‘production’ dataset, warehouse and administrator functions, and handling SQL
injection attacks. Lucas Carter worked on all aspects of the seller page and the add/edit listing
page. Sergio Wallace-Vera worked on the search bar, the recommended items, the items page,
the sellers display/add cart on the item page, and the reviews display/add review on the item
page. Sergio also worked on acquiring, cleaning, and creating the ‘production’ datasets.
 
