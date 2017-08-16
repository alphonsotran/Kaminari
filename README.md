# Kaminari 
------------------------------------------------------------------------------
A Scope & Engine based, clean, powerful, customizable and sophisticated paginator for modern web app frameworks and ORMs. Essentially, it adds pages to your index page. 

## Installation
------------------------------------------------------------------------------
Include the gem in your gemfile.
```
gem 'kaminari'
```

## Controllers
-------------------------------------------------------------------------------
```
@users = User.order(:name).page(params[:page])
```

## Views
-------------------------------------------------------------------------------
```
<%= paginate @users %>
```

## Query Basics
-------------------------------------------------------------------------------

Set queries in your index show page. 

### Page Scope
```
User.count                     #=> 1000
User.page(1).limit_value       #=> 20
User.page(1).total_pages       #=> 50
User.page(1).current_page      #=> 1
User.page(1).next_page         #=> 2
User.page(2).prev_page         #=> 1
User.page(1).first_page?       #=> true
User.page(50).last_page?       #=> true
User.page(100).out_of_range?   #=> true
```

### Per Scope
```
User.page(7).per(50)
```
