> # It's a backend API of a restaurant apps .


<!-- ![plot](https://www.figma.com/file/ogSnH6FFEPdbrcnjvXsSHW/Untitled-(Copy)?node-id=0%3A1&t=rBa9SuUeaQ0GW2I1-0) -->
![216312854-28c4a9f8-e3f0-4ae7-815c-2835b6f1c9e1](https://user-images.githubusercontent.com/85397106/231838848-61912eb2-cd36-4ced-9d2a-f7bdd7dc6ea9.png)




# **Restaurant**:
> ### restaurant_signup ******
- id
- username
- name
- email
- phone number
- address
- password\
(show signup successful)
> ### restaurant_signin ******
  - email
  - password
  (show signed in successfully)
 >### add_items ******
  - item name
  - item description
  - item price
  - item cooking time
  - item quantity
  - ForeignKey('restaurant_signup.id')
    (items added successfully)
> ### get_customer_ordered_dishes ******
  - restaurant_id\
  (show order details of current restaurant)

# **User**:
> ### customer_signup ******
  - id
  - name
  - email
  - phone number
  - address
  - password\
  (signup successful)
>### customer_signin ******
  - username
  - password\
  (signed in successfully)
> ### choose_restaurant ******
  - restaurant_name\
  (if restaurant_name not match --> restaurant not available)\
  (if restaurant_name matched --> show available dishes and its rating)
> ### choose_dishes_place_order ******
  - restaurant_name
  - dish_name
  - quantity
  - delivery_address
  - ForeignKey('customer_signup.id')
  
  (if quantity not available then show the available quantity) \
  (if quantity available show dishes are available.)\
  (Order successful. Payment should be done in cash to the delivery person.)
> ### check ordered history of customers
  - username
  >show dictionary of oredered history of customers where keys are 
  ```
  >- restaurant_name
  >- dish_name
  >- quantity
  >- price
  >- Total_price
  >- delivery_address
  ```
> ### delivery
- restaurant_name\
  (it will be deleted the first order from the customer order table of the specific restaurant and show it's delivered order successfully)
> ###  give_rating_feedback *****
  - restaurant_name
  - customer_name
  - item_name
  - item_rating
  - item_feedback \
  (Thanks for your feedback)
